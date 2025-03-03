---
UID: NS:dispmprt._DXGKARG_CREATEVIRTUALGPU
title: _DXGKARG_CREATEVIRTUALGPU
description: Arguments used to create a virtual GPU.
tech.root: display
ms.date: 04/04/2019
keywords: ["DXGKARG_CREATEVIRTUALGPU structure"]
ms.keywords: _DXGKARG_CREATEVIRTUALGPU, DXGKARG_CREATEVIRTUALGPU, *PDXGKARG_CREATEVIRTUALGPU,
req.header: dispmprt.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: DXGKARG_CREATEVIRTUALGPU, *PDXGKARG_CREATEVIRTUALGPU
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - _DXGKARG_CREATEVIRTUALGPU
 - dispmprt/_DXGKARG_CREATEVIRTUALGPU
 - PDXGKARG_CREATEVIRTUALGPU
 - dispmprt/PDXGKARG_CREATEVIRTUALGPU
 - DXGKARG_CREATEVIRTUALGPU
 - dispmprt/DXGKARG_CREATEVIRTUALGPU
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dispmprt.h
api_name:
 - _DXGKARG_CREATEVIRTUALGPU
 - PDXGKARG_CREATEVIRTUALGPU
 - DXGKARG_CREATEVIRTUALGPU
product:
 - Windows
dev_langs:
 - c++
---

# _DXGKARG_CREATEVIRTUALGPU structure


## -description

Arguments used to create a virtual GPU.

## -struct-fields

### -field PartitionId

An index (from 0 to maximum supported vGPU minus one) for the vGPU partition.

### -field Profile

Describes the desired vGPU capabilities.

### -field UserModeVirtualDeviceProvider

The class Id for the user mode emulation DLL. This value can be set to zero if the driver does not need device emulation. The Id is used by the OS to instantiate the user mode DLL.

### -field VirtualGpuLuid

LUID, which uniquely identifies the virtual GPU. This LUID will be passed to the user mode emulation DLL.

### -field NumMemorySegments

The number of valid entries in the *SegmentInfo* array.

### -field SegmentInfo

First *NumMemorySegment* entries describe information about local memory segments, which are needed in the vGPU.

### -field NumEngines

The number of valid elements in the EngineInfo array.  This is deprecated and should be zero.

### -field EngineInfo

 
Specifies physical engines, which should be used when creating a vGPU with the given profile. This is deprecated and should be zero.

## -remarks

## -see-also

