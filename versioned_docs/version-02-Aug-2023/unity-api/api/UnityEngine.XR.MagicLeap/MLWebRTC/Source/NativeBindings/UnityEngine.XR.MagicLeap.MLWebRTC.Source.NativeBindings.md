---
title: NativeBindings
summary: native bindings for the mlwebrtc.source struct. 

---

# NativeBindings




Native bindings for the MLWebRTC.Source struct.   


Inherits from: <br></br>[MagicLeapNativeBindings](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap.Native/MagicLeapNativeBindings/UnityEngine.XR.MagicLeap.Native.MagicLeapNativeBindings.md)




## Public Methods

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceCreateAppDefinedAudioSourceEx {#mlresultcode-mlwebrtcsourcecreateappdefinedaudiosourceex}

Creates the local source with the specified parameters. 

```csharp
public MLResult.Code MLWebRTCSourceCreateAppDefinedAudioSourceEx(
    ref MLWebRTCAppDefinedSourceParams sourceParams,
    out ulong sourceHandle
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ref [MLWebRTCAppDefinedSourceParams](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/MLWebRTC/Source/NativeBindings/UnityEngine.XR.MagicLeap.MLWebRTC.Source.NativeBindings.MLWebRTCAppDefinedSourceParams.md) |sourceParams|Audio source parameters|
| out ulong |sourceHandle|The handle to the local source to return to the caller.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the local source was successfully created. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceCreateLocalSourceForCamera {#mlresultcode-mlwebrtcsourcecreatelocalsourceforcamera}

Creates the local source that links to the user's MLCamera. 

```csharp
public MLResult.Code MLWebRTCSourceCreateLocalSourceForCamera(
    in MLCamera.NativeBindings.MLCameraConnectContext inputContext,
    out ulong sourceHandle
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| in MLCamera.NativeBindings.MLCameraConnectContext |sourceHandle|The handle to the local source to return to the caller.|
| out ulong |sourceHandle||






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the local source was successfully created. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceCreateLocalSourceForMicrophoneEx {#mlresultcode-mlwebrtcsourcecreatelocalsourceformicrophoneex}

Creates the local source with the specified track name that links to the user's microphone. 

```csharp
public MLResult.Code MLWebRTCSourceCreateLocalSourceForMicrophoneEx(
    string trackName,
    out ulong sourceHandle
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| string |trackName|Track name|
| out ulong |sourceHandle|The handle to the local source to return to the caller.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the local source was successfully created. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceDestroy {#mlresultcode-mlwebrtcsourcedestroy}

Destroys the local source. 

```csharp
public MLResult.Code MLWebRTCSourceDestroy(
    ulong sourceHandle
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle to the local source to destroy.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the local source was successfully destroyed. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceGetTrackId {#mlresultcode-mlwebrtcsourcegettrackid}

Gets the track Id of a source, call MLWebRTCSourceReleaseTrackId after. 

```csharp
public MLResult.Code MLWebRTCSourceGetTrackId(
    ulong sourceHandle,
    out IntPtr trackIdPtr
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle of the media source.|
| out IntPtr |trackIdPtr|Double-pointer to the unmanaged trackId string.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if destroying all handles was successful. MLResult.Result will be  MLResult.Code.MismatchingHandle  if an incorrect handle was sent. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceGetType {#mlresultcode-mlwebrtcsourcegettype}

Checks if an video source is currently enabled. 

```csharp
public MLResult.Code MLWebRTCSourceGetType(
    ulong sourceHandle,
    out MLWebRTC.MediaStream.Track.Type sourceType
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle of the video source.|
| out [MLWebRTC.MediaStream.Track.Type](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/MLWebRTC/MediaStream/UnityEngine.XR.MagicLeap.MLWebRTC.MediaStream.Track.md#enums-type) |sourceType|Type of the source.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the video source status was queried successfully. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceIsEnabled {#mlresultcode-mlwebrtcsourceisenabled}

Checks if an audio source is currently enabled. 

```csharp
public MLResult.Code MLWebRTCSourceIsEnabled(
    ulong sourceHandle,
    out bool enabled
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle of the source.|
| out bool |enabled|True if source is enabled.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the audio source status was queried successfully. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceReleaseTrackId {#mlresultcode-mlwebrtcsourcereleasetrackid}

Releases the memory created when calling MLWebRTCSourceGetTrackId. 

```csharp
public MLResult.Code MLWebRTCSourceReleaseTrackId(
    ulong sourceHandle,
    IntPtr trackId
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle of the data channel.|
| IntPtr |trackId|Pointer to the unmanaged trackId string.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if destroying all handles was successful. MLResult.Result will be  MLResult.Code.MismatchingHandle  if an incorrect handle was sent. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

### [MLResult.Code](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/UnityEngine.XR.MagicLeap.MLResult.md#int-code) MLWebRTCSourceSetEnabled {#mlresultcode-mlwebrtcsourcesetenabled}

Enables or disables a audio source. 

```csharp
public MLResult.Code MLWebRTCSourceSetEnabled(
    ulong sourceHandle,
    bool enabled
)
```


**Parameters**

| Type | Name  | Description  | 
|--|--|--|
| ulong |sourceHandle|The handle of the audio source.|
| bool |enabled|Sets the audio source to be enabled or disabled.|






**Returns**: MLResult.Result will be  MLResult.Code.Ok  if the audio source was enabled/disabled successfully. MLResult.Result will be  MLResult.Code.PermissionDenied  if necessary permission is missing. MLResult.Result will be  MLResult.Code.UnspecifiedFailure  if failed due to other internal error. 



-----------

