---

title: MagicLeapFeature.cs

---


# MagicLeapFeature.cs









## Source code

```csharp
// %BANNER_BEGIN%
// ---------------------------------------------------------------------
// %COPYRIGHT_BEGIN%
// Copyright (c) (2019-2022) Magic Leap, Inc. All Rights Reserved.
// Use of this file is governed by the Software License Agreement, located here: https://www.magicleap.com/software-license-agreement-ml2
// Terms and conditions applicable to third-party materials accompanying this distribution may also be found in the top-level NOTICE file appearing herein.
// %COPYRIGHT_END%
// ---------------------------------------------------------------------
// %BANNER_END%
#if UNITY_OPENXR_1_7_0_OR_NEWER
using System.Collections.Generic;
using UnityEngine.XR.ARSubsystems;
using UnityEngine.XR.MagicLeap;
using System;
#if UNITY_EDITOR
using UnityEditor;
using UnityEditor.XR.OpenXR.Features;
#endif

namespace UnityEngine.XR.OpenXR.Features.MagicLeapSupport
{
#if UNITY_EDITOR
    [OpenXRFeature(UiName = "Magic Leap 2 Support",
        Desc="Necessary to deploy a Magic Leap 2 compatible application.",
        Company = "Magic Leap",
        Version = "1.0.0",
        BuildTargetGroups = new []{ BuildTargetGroup.Android, BuildTargetGroup.Standalone },
        CustomRuntimeLoaderBuildTargets = new []{ BuildTarget.Android },
        FeatureId = featureId,
        OpenxrExtensionStrings = "XR_ML_compat " +
                                 "XR_ML_frame_end_info " +
                                 "XR_ML_global_dimmer " +
                                 "XR_EXT_view_configuration_depth_range " +
                                 "XR_KHR_convert_timespec_time"
    )]
#endif
    public partial class MagicLeapFeature : OpenXRFeature
    {
        private struct xrSessionCached
        {
            public int oldState;
            public int newState;
        }
        
        public const string featureId = "com.magicleap.openxr.feature.ml2";

        [SerializeField]
        private bool enableMLAudio = false;

        public bool IsMLAudioEnabled => enableMLAudio;

        private static List<XRMeshSubsystemDescriptor> s_MeshSubsysDesc = new List<XRMeshSubsystemDescriptor>();
        private static List<XRPlaneSubsystemDescriptor> s_PlaneSubsysDesc = new List<XRPlaneSubsystemDescriptor>();
        private static List<XRSessionSubsystemDescriptor> s_SessionSubsysDesc = new List<XRSessionSubsystemDescriptor>();

        public delegate void OnXRSessionStateChangeDelegate(int oldState, int newState);
        public static event OnXRSessionStateChangeDelegate OnXRSessionStateChange;

        private static List<xrSessionCached> xrSessionCacheList;

        protected override IntPtr HookGetInstanceProcAddr(IntPtr func)
        {
            return NativeBindings.MLOpenXRInterceptFunctions(func);
        }

        protected override bool OnInstanceCreate(ulong xrInstance)
        {
            return NativeBindings.MLOpenXROnInstanceCreate(xrGetInstanceProcAddr, xrInstance);
        }

        protected override void OnInstanceDestroy(ulong xrInstance)
        {
            NativeBindings.MLOpenXROnInstanceDestroy(xrInstance);
        }

        protected override void OnAppSpaceChange(ulong xrSpace)
        {
            NativeBindings.MLOpenXROnAppSpaceChange(xrSpace);
        }

        protected override void OnSessionCreate(ulong xrSession)
        {
            NativeBindings.MLOpenXROnSessionCreate(xrSession);
        }

        protected override void OnSessionDestroy(ulong xrSession)
        {
            NativeBindings.MLOpenXROnSessionDestroy(xrSession);
        }
        protected override void OnSessionStateChange(int oldState, int newState)
        {
            if (OnXRSessionStateChange != null)
            {
                OnXRSessionStateChange.Invoke(oldState, newState);
            }
            else
            {
                xrSessionCached newEvent;
                newEvent.oldState = oldState;
                newEvent.newState = newState;

                xrSessionCacheList.Add(newEvent);
            }
        }

        protected override void OnSubsystemCreate()
        {
            xrSessionCacheList = new List<xrSessionCached>();

            base.OnSubsystemCreate();

            CreateSubsystem<XRPlaneSubsystemDescriptor, XRPlaneSubsystem>(s_PlaneSubsysDesc, MagicLeapXrProvider.PlanesSubsystemId);
            CreateSubsystem<XRMeshSubsystemDescriptor, XRMeshSubsystem>(s_MeshSubsysDesc, MagicLeapXrProvider.MeshingSubsystemId);
            CreateSubsystem<XRSessionSubsystemDescriptor, XRSessionSubsystem>(s_SessionSubsysDesc, MagicLeapXrProvider.SessionSubsystemId);
        }

        protected override void OnSubsystemStart()
        {
            base.OnSubsystemStart();

            StartSubsystem<XRPlaneSubsystem>();
        }

        protected override void OnSubsystemStop()
        {
            base.OnSubsystemStop();

            StopSubsystem<XRPlaneSubsystem>();
        }

        protected override void OnSubsystemDestroy()
        {
            base.OnSubsystemDestroy();

            DestroySubsystem<XRPlaneSubsystem>();
            DestroySubsystem<XRMeshSubsystem>();
            DestroySubsystem<XRSessionSubsystem>();
        }

        public void StartMeshSubsystem()
        {
            StartSubsystem<XRMeshSubsystem>();
        }

        public void StopMeshSubsystem()
        {
            StopSubsystem<XRMeshSubsystem>();
        }

        public static void GetCachedSessionEvents()
        {
            foreach (xrSessionCached cachedEvent in xrSessionCacheList)
            {
                OnXRSessionStateChange.Invoke(cachedEvent.oldState, cachedEvent.newState);
            }

            xrSessionCacheList.Clear();
        }
    }
}
#endif
```




