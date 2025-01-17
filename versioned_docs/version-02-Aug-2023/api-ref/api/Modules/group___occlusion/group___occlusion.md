---
title: Occlusion
summary: experimental this is an experimental api which may be modified or removed without any prior notice. 

---

# Occlusion

APIs for the Occlusion system. \experimental This is an experimental API which may be modified or removed without any prior notice.  [More...](#detailed-description)

## Classes

|                | Name           |
| -------------- | -------------- |
| struct | **[MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md)** <br></br>Mesh Settings for the underlying system.  |
| struct | **[MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md)** <br></br>Structure for occlusion mesh data.  |
| struct | **[MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md)** <br></br>Structure for occlusion mesh query.  |

## Types

|                | Name           |
| -------------- | -------------- |
| typedef struct [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) | **[MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#struct-mlocclusionsettings)** <br></br>Mesh Settings for the underlying system.  |
| typedef struct [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) | **[MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#struct-mlocclusionmesh)** <br></br>Structure for occlusion mesh data.  |
| typedef struct [MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) | **[MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#struct-mlocclusionmeshquery)** <br></br>Structure for occlusion mesh query.  |

## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[MLOcclusionSettingsInit](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#void-mlocclusionsettingsinit)**([MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * inout_settings)<br></br>Initialize the occlusion settings with system defaults.  |
| void | **[MLOcclusionMeshInit](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#void-mlocclusionmeshinit)**([MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * inout_mesh)<br></br>Initialize the occlusion mesh with system defaults.  |
| void | **[MLOcclusionMeshQueryInit](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#void-mlocclusionmeshqueryinit)**([MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) * inout_mesh_query)<br></br>Initialize the occlusion mesh query with system defaults.  |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) | **[MLOcclusionCreateClient](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusioncreateclient)**(const [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * settings, [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) * out_client_handle)<br></br>Create the occlusion client.  |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) | **[MLOcclusionDestroyClient](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusiondestroyclient)**([MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) client_handle)<br></br>Free the client resources.  |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) | **[MLOcclusionUpdateSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusionupdatesettings)**([MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) handle, const [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * settings)<br></br>Update the occlusion settings at runtime.  |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) | **[MLOcclusionGetLatestMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusiongetlatestmesh)**([MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) handle, const [MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) * mesh_query, [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * out_mesh_data)<br></br>Get the latest occlusion mesh.  |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) | **[MLOcclusionReleaseMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusionreleasemesh)**([MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) handle, [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * mesh_data)<br></br>Releases specified [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) object.  |

## Detailed Description

APIs for the Occlusion system. \experimental This is an experimental API which may be modified or removed without any prior notice. 




**Shared Object:**
  * perception.magicleap*

* The Occlusion system is for generating a mesh representation of the near field objects, so they can be easily used for occlusion of in-app objects for greater immersion. 




-----------

## Types Documentation

### MLOcclusionSettings {#struct-mlocclusionsettings}

```cpp
typedef struct MLOcclusionSettings MLOcclusionSettings;
```

Mesh Settings for the underlying system. 



[More Info](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md)


**API Level:**
  * 28




-----------

### MLOcclusionMesh {#struct-mlocclusionmesh}

```cpp
typedef struct MLOcclusionMesh MLOcclusionMesh;
```

Structure for occlusion mesh data. 



[More Info](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md)


**API Level:**
  * 28




-----------

### MLOcclusionMeshQuery {#struct-mlocclusionmeshquery}

```cpp
typedef struct MLOcclusionMeshQuery MLOcclusionMeshQuery;
```

Structure for occlusion mesh query. 



[More Info](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md)


**API Level:**
  * 28




-----------


## Functions Documentation

### MLOcclusionSettingsInit {#void-mlocclusionsettingsinit}

```cpp
static inline void MLOcclusionSettingsInit(
    MLOcclusionSettings * inout_settings
)
```

Initialize the occlusion settings with system defaults. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * |inout_settings|The initial settings to be used for occlusion.|
**Required Permissions**:

  * None 





**API Level:**
  * 28




-----------

### MLOcclusionMeshInit {#void-mlocclusionmeshinit}

```cpp
static inline void MLOcclusionMeshInit(
    MLOcclusionMesh * inout_mesh
)
```

Initialize the occlusion mesh with system defaults. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * |inout_mesh|The initial mesh structure.|
**Required Permissions**:

  * None 





**API Level:**
  * 28




-----------

### MLOcclusionMeshQueryInit {#void-mlocclusionmeshqueryinit}

```cpp
static inline void MLOcclusionMeshQueryInit(
    MLOcclusionMeshQuery * inout_mesh_query
)
```

Initialize the occlusion mesh query with system defaults. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) * |inout_mesh_query|The initial mesh query structure.|
**Required Permissions**:

  * None 





**API Level:**
  * 28




-----------

### MLOcclusionCreateClient {#mlresult-mlocclusioncreateclient}

```cpp
MLResult MLOcclusionCreateClient(
    const MLOcclusionSettings * settings,
    MLHandle * out_client_handle
)
```

Create the occlusion client. 

**Parameters**

|  |   |   |
|--|--|--|
| const [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * |settings|The initial settings to be used for occlusion. |
| [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) * |out_client_handle|The handle to the created client.|

**Returns**

|  |   |   |
|--|--|--|
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_InvalidParam|Occlusion client was not created due to an invalid parameter. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_Ok|Occlusion client was created successfully. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_PerceptionSystemNotStarted|Perception System has not been started. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_PermissionDenied|Missing required permission(s). |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_UnspecifiedFailure|Occlusion client was not created due to an unknown error.|
**Required Permissions**:

  * com.magicleap.permission.SPATIAL_MAPPING (protection level: dangerous) 





**API Level:**
  * 28




-----------

### MLOcclusionDestroyClient {#mlresult-mlocclusiondestroyclient}

```cpp
MLResult MLOcclusionDestroyClient(
    MLHandle client_handle
)
```

Free the client resources. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) |client_handle|The client to destroy.|

**Returns**

|  |   |   |
|--|--|--|
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_InvalidParam|Occlusion client was not destroyed due to an invalid parameter. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_Ok|Occlusion client was destroyed successfully. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_PerceptionSystemNotStarted|Perception System has not been started.|
**Required Permissions**:

  * None 





**API Level:**
  * 28




-----------

### MLOcclusionUpdateSettings {#mlresult-mlocclusionupdatesettings}

```cpp
MLResult MLOcclusionUpdateSettings(
    MLHandle handle,
    const MLOcclusionSettings * settings
)
```

Update the occlusion settings at runtime. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) |handle|The handle to the created client. |
| const [MLOcclusionSettings](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_settings.md) * |settings|The updated settings to be used for occlusion.|

**Returns**

|  |   |   |
|--|--|--|
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_InvalidParam|Settings were not updated due to an invalid parameter. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_Ok|Settings were updated successfully. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_PerceptionSystemNotStarted|Perception System has not been started.|
**Required Permissions**:

  * None 





**API Level:**
  * 28




-----------

### MLOcclusionGetLatestMesh {#mlresult-mlocclusiongetlatestmesh}

```cpp
MLResult MLOcclusionGetLatestMesh(
    MLHandle handle,
    const MLOcclusionMeshQuery * mesh_query,
    MLOcclusionMesh * out_mesh_data
)
```

Get the latest occlusion mesh. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) |handle|The handle to the created client. |
| const [MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) * |mesh_query|The pointer to intialized [MLOcclusionMeshQuery](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh_query.md) struct. |
| [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * |out_mesh_data|The pointer to intialized [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) struct.|

**Returns**

|  |   |   |
|--|--|--|
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_IllegalState|Current mesh must be released before acquiring the next one. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_InvalidParam|Mesh data was not returned due to an invalid parameter. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_Ok|Mesh data was returned successfully. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_PerceptionSystemNotStarted|Perception System has not been started.|
**Required Permissions**:

  * None 


Returns [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) with its latest data. When doing consecutive calls and there was no mesh update, the same data will be returned. The memory is owned by the system. Application should copy the data it needs to cache.

Every call to [MLOcclusionGetLatestMesh()](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusiongetlatestmesh) must be followed by a matching call to [MLOcclusionReleaseMesh()](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusionreleasemesh), otherwise this method will return an error.




**API Level:**
  * 28




-----------

### MLOcclusionReleaseMesh {#mlresult-mlocclusionreleasemesh}

```cpp
MLResult MLOcclusionReleaseMesh(
    MLHandle handle,
    MLOcclusionMesh * mesh_data
)
```

Releases specified [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) object. 

**Parameters**

|  |   |   |
|--|--|--|
| [MLHandle](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#uint64-t-mlhandle) |handle|The handle to the created client. |
| [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) * |mesh_data|Pointer to a filled [MLOcclusionMesh](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/struct_m_l_occlusion_mesh.md) struct.|

**Returns**

|  |   |   |
|--|--|--|
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_InvalidParam|One of the parameters is invalid. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_Ok|Successfully released mesh data. |
| [MLResult](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___platform/group___platform.md#int32-t-mlresult) |MLResult_UnspecifiedFailure|Failed due to an internal error.|
**Required Permissions**:

  * None 


This function should be called exactly once for each call to [MLOcclusionGetLatestMesh()](/versioned_docs/version-02-Aug-2023/api-ref/api/Modules/group___occlusion/group___occlusion.md#mlresult-mlocclusiongetlatestmesh). After a successful call, the contents of #mesh_data are no longer valid and should not be used.




**API Level:**
  * 28




-----------






