---
UID: NS:d3dkmddi._DXGKARGCB_MAPCONTEXTALLOCATION
title: _DXGKARGCB_MAPCONTEXTALLOCATION (d3dkmddi.h)
description: DXGKARGCB_MAPCONTEXTALLOCATION is used with DxgkCbMapContextAllocation to map a graphics processing unit (GPU) virtual address to the specified context allocation.
old-location: display\dxgkargcb_mapcontextallocation.htm
ms.date: 05/10/2018
keywords: ["DXGKARGCB_MAPCONTEXTALLOCATION structure"]
ms.keywords: DXGKARGCB_MAPCONTEXTALLOCATION, DXGKARGCB_MAPCONTEXTALLOCATION structure [Display Devices], _DXGKARGCB_MAPCONTEXTALLOCATION, d3dkmddi/DXGKARGCB_MAPCONTEXTALLOCATION, display.dxgkargcb_mapcontextallocation
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
tech.root: display
req.typenames: DXGKARGCB_MAPCONTEXTALLOCATION
f1_keywords:
 - _DXGKARGCB_MAPCONTEXTALLOCATION
 - d3dkmddi/_DXGKARGCB_MAPCONTEXTALLOCATION
 - DXGKARGCB_MAPCONTEXTALLOCATION
 - d3dkmddi/DXGKARGCB_MAPCONTEXTALLOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGKARGCB_MAPCONTEXTALLOCATION
 - DXGKARGCB_MAPCONTEXTALLOCATION
---

# _DXGKARGCB_MAPCONTEXTALLOCATION structure


## -description

<b>DXGKARGCB_MAPCONTEXTALLOCATION</b> is used with <a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkcb_mapcontextallocation">DxgkCbMapContextAllocation</a> to map a graphics processing unit (GPU) virtual address to the specified context allocation.

## -struct-fields

### -field BaseAddress

(optional) If non-NULL, the video memory manager will attempt to use this address as the base address for the mapping. If the range from <b>BaseAddress</b> to <b>BaseAddress</b>+<b>Size</b> isn’t free, the call will fail. When this parameter is non-NULL, <b>MinimumAddress</b> and <b>MaximumAddress</b> are ignored.



If NULL is specified, the video memory manager will pick the base address for the allocation within the specified <b>MinimumAddress</b> and <b>MaximumAddress</b>.

### -field MinimumAddress

(optional) Specifies the minimum GPU virtual address to consider for the mapped range. 


This parameter is ignored when <b>BaseAddress</b> != <b>NULL</b>.

### -field MaximumAddress

Specifies the maximum GPU virtual address to consider for the mapped range. The video memory manager will guarantee that <b>BaseAddress</b>+<b>Size</b> <= <b>MaximumAddress</b>. If this is set to <b>NULL</b> the video memory manager will not apply any limit.


This parameter is ignored when <b>BaseAddress</b> != <b>NULL</b>.

### -field hAllocation

Handle to the allocation being mapped into the GPU virtual address space. This is a DirectX graphics kernel  handle, returned by <a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkcb_createcontextallocation">DxgkCbCreateContextAllocation</a>.

### -field OffsetInPages

Specifies the offset, in 4KB pages, to the starting page within the specified allocation that must be mapped.

### -field SizeInPages

Specifies the size of the range to map in number of 4KB pages.

### -field Protection

Specifies the protection on the GPU virtual address that is mapped.

### -field DriverProtection

Specifies the driver protection parameters.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkcb_createcontextallocation">DxgkCbCreateContextAllocation</a>



<a href="/windows-hardware/drivers/ddi/d3dkmddi/nc-d3dkmddi-dxgkcb_mapcontextallocation">DxgkCbMapContextAllocation</a>

