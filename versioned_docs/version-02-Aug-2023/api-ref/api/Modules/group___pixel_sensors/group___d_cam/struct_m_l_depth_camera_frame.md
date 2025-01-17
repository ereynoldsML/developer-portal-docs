---
title: MLDepthCameraFrame
summary: structure to encapsulate output data for each camera sensor. 

---

# MLDepthCameraFrame

**Module:** **[Pixel Sensors](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___pixel_sensors.md)** **/** **[Depth Camera](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md)**



Structure to encapsulate output data for each camera sensor.  [More...](#detailed-description)


`#include <ml_depth_camera.h>`

## Public Attributes

| Type           | Name           |
| -------------- | -------------- |
| int64_t | **[frame_number](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#int64-t-frame-number)**  |
| [MLTime](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___common/group___common.md#int64-t-mltime) | **[frame_timestamp](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mltime-frame-timestamp)**  |
| [MLDepthCameraFrameType](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#enums-mldepthcameraframetype) | **[frame_type](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameraframetype-frame-type)**  |
| [MLTransform](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___common/struct_m_l_transform.md) | **[camera_pose](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mltransform-camera-pose)**  |
| [MLDepthCameraIntrinsics](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_intrinsics.md) | **[intrinsics](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameraintrinsics-intrinsics)**  |
| [MLDepthCameraDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameradepthimage) * | **[depth_image](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameradepthimage-depth-image)**  |
| [MLDepthCameraConfidenceBuffer](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameraconfidencebuffer) * | **[confidence](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameraconfidencebuffer-confidence)**  |
| [MLDepthCameraDepthFlagsBuffer](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameradepthflagsbuffer) * | **[flags](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameradepthflagsbuffer-flags)**  |
| [MLDepthCameraAmbientRawDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameraambientrawdepthimage) * | **[ambient_raw_depth_image](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcameraambientrawdepthimage-ambient-raw-depth-image)** <br></br>Ambient raw depth image. The illuminator in the sensor is modulated with a system determined frequency. This is the raw sensor data captured when the illuminator is off.  |
| [MLDepthCameraRawDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcamerarawdepthimage) * | **[raw_depth_image](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_frame.md#mldepthcamerarawdepthimage-raw-depth-image)** <br></br>Raw depth image. The illuminator in the sensor is modulated with a system determined frequency. This is the raw sensor data captured when the illuminator is on.  |

## Detailed Description

```cpp
struct MLDepthCameraFrame;
```

Structure to encapsulate output data for each camera sensor. 




**API Level:**
  * 29




-----------
## Public Attributes Documentation

### frame_number {#int64-t-frame-number}

```cpp
int64_t frame_number;
```


A 64bit integer to index the frame number associated with this frame. 





-----------

### frame_timestamp {#mltime-frame-timestamp}

```cpp
MLTime frame_timestamp;
```


Frame timestamp specifies the time at which the frame was captured. 





-----------

### frame_type {#mldepthcameraframetype-frame-type}

```cpp
MLDepthCameraFrameType frame_type;
```



| Type | Description |
|--|--|
| [MLDepthCameraFrameType](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#enums-mldepthcameraframetype) | Enumeration of camera stream used when capturing a frame.  |


Depth camera stream used for capturing this frame. 





-----------

### camera_pose {#mltransform-camera-pose}

```cpp
MLTransform camera_pose;
```


Depth camera pose in the world co-ordinate system. 





-----------

### intrinsics {#mldepthcameraintrinsics-intrinsics}

```cpp
MLDepthCameraIntrinsics intrinsics;
```



| Type | Description |
|--|--|
| [MLDepthCameraIntrinsics](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/struct_m_l_depth_camera_intrinsics.md) | Depth camera intrinsic parameters.  |


Camera intrinsic parameters. 





-----------

### depth_image {#mldepthcameradepthimage-depth-image}

```cpp
MLDepthCameraDepthImage * depth_image;
```



| Type | Description |
|--|--|
| [MLDepthCameraDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameradepthimage) * | Depth image.  |


Depth image. 





-----------

### confidence {#mldepthcameraconfidencebuffer-confidence}

```cpp
MLDepthCameraConfidenceBuffer * confidence;
```



| Type | Description |
|--|--|
| [MLDepthCameraConfidenceBuffer](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameraconfidencebuffer) * | Confidence score.  |


Confidence score. 





-----------

### flags {#mldepthcameradepthflagsbuffer-flags}

```cpp
MLDepthCameraDepthFlagsBuffer * flags;
```



| Type | Description |
|--|--|
| [MLDepthCameraDepthFlagsBuffer](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameradepthflagsbuffer) * | Flags.  |


Depth flags. 





-----------

### ambient_raw_depth_image {#mldepthcameraambientrawdepthimage-ambient-raw-depth-image}

```cpp
MLDepthCameraAmbientRawDepthImage * ambient_raw_depth_image;
```

Ambient raw depth image. The illuminator in the sensor is modulated with a system determined frequency. This is the raw sensor data captured when the illuminator is off. 


| Type | Description |
|--|--|
| [MLDepthCameraAmbientRawDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcameraambientrawdepthimage) * | Ambient raw depth image.  |






-----------

### raw_depth_image {#mldepthcamerarawdepthimage-raw-depth-image}

```cpp
MLDepthCameraRawDepthImage * raw_depth_image;
```

Raw depth image. The illuminator in the sensor is modulated with a system determined frequency. This is the raw sensor data captured when the illuminator is on. 


| Type | Description |
|--|--|
| [MLDepthCameraRawDepthImage](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___pixel_sensors/group___d_cam/group___d_cam.md#mldepthcameraframebuffer-mldepthcamerarawdepthimage) * | Raw depth image.  |






-----------


