---
title: MLDepthCameraCapabilityList
summary: structure to encapsulate a list of possible stream configurations. user should be able to use any of the capabilities from the list. they are grouped in usable sets of configurations - one set may contain different mldepthcamerastreamcapability for different streams. for more information see mldepthcameracapability. 

---

# MLDepthCameraCapabilityList




Structure to encapsulate a list of possible stream configurations. User should be able to use any of the capabilities from the list. They are grouped in usable sets of configurations - one set may contain different MLDepthCameraStreamCapability for different streams. For more information see MLDepthCameraCapability.   





## Public Attributes

### Capabilities {#intptr-capabilities}

Array of MLDepthCameraCapability elements. 

```csharp

public IntPtr Capabilities;

```






-----------

### Size {#byte-size}

Size of Capabilities array. 

```csharp

public byte Size;

```






-----------


