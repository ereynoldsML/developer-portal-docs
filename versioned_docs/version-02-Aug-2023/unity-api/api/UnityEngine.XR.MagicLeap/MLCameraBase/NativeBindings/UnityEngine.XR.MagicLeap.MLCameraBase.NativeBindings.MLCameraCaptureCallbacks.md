---
title: MLCameraCaptureCallbacks
summary: capture callbacks to be implemented by client to receive capture status if callback mechanism is used. this structure must be initialized by calling mlcameracapturecallbacksinit before use. 

---

# MLCameraCaptureCallbacks




Capture callbacks to be implemented by client to receive capture status if callback mechanism is used. This structure must be initialized by calling MLCameraCaptureCallbacksInit() before use.   





## Public Methods

### [MLCameraCaptureCallbacks](/versioned_docs/version-02-Aug-2023/unity-api/api/UnityEngine.XR.MagicLeap/MLCameraBase/NativeBindings/UnityEngine.XR.MagicLeap.MLCameraBase.NativeBindings.MLCameraCaptureCallbacks.md) Create {#mlcameracapturecallbacks-create}

Create and return an initialized version of this struct. 

```csharp
public static MLCameraCaptureCallbacks Create()
```






**Returns**: A new instance of this struct.



-----------

## Public Attributes

### OnCaptureAborted {#oncaptureaborteddelegate-oncaptureaborted}

Callback is invoked when an ongoing video or preview capture or both are aborted due to an error. 

```csharp

public OnCaptureAbortedDelegate OnCaptureAborted;

```






-----------

### OnCaptureCompleted {#oncapturecompleteddelegate-oncapturecompleted}

Callback is invoked when capturing single frame is completed and result is available. 

```csharp

public OnCaptureCompletedDelegate OnCaptureCompleted;

```






-----------

### OnCaptureFailed {#oncapturefaileddelegate-oncapturefailed}

Callback is invoked when a capture has failed when the camera device failed to produce a capture result for the request. 

```csharp

public OnCaptureFailedDelegate OnCaptureFailed;

```






-----------

### OnImageBufferAvailable {#onimagebufferavailabledelegate-onimagebufferavailable}

Callback is invoked when a captured image buffer is available with #MLCameraCaptureType&#95;ImageRaw. 

```csharp

public OnImageBufferAvailableDelegate OnImageBufferAvailable;

```






-----------

### OnPreviewBufferAvailable {#onpreviewbufferavailabledelegate-onpreviewbufferavailable}

Callback is invoked when a preview video frame buffer is available with #MLCameraCaptureType&#95;Preview. 

```csharp

public OnPreviewBufferAvailableDelegate OnPreviewBufferAvailable;

```






-----------

### OnVideoBufferAvailable {#onvideobufferavailabledelegate-onvideobufferavailable}

Callback is invoked when a captured raw/compressed video frame buffer is available with #MLCameraCaptureType&#95;VideoRaw. 

```csharp

public OnVideoBufferAvailableDelegate OnVideoBufferAvailable;

```






-----------

### Version {#uint-version}

version contains the version number for this structure. 

```csharp

public uint Version;

```






-----------


