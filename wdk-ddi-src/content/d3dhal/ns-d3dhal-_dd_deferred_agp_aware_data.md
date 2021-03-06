---
UID: NS:d3dhal._DD_DEFERRED_AGP_AWARE_DATA
title: _DD_DEFERRED_AGP_AWARE_DATA (d3dhal.h)
description: DirectX 8.0 and later versions and NT-based operating systems only. DD_DEFERRED_AGP_AWARE_DATA is the data structure pointed to by the lpvData field of DD_GETDRIVERINFODATA for D3DGDI2_TYPE_DEFERRED_AGP_AWARE notifications.
old-location: display\dd_deferred_agp_aware_data.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["DD_DEFERRED_AGP_AWARE_DATA structure"]
ms.keywords: DD_DEFERRED_AGP_AWARE_DATA, DD_DEFERRED_AGP_AWARE_DATA structure [Display Devices], _DD_DEFERRED_AGP_AWARE_DATA, d3dhal/DD_DEFERRED_AGP_AWARE_DATA, d3dstrct_f07b3180-3442-4c3f-974b-eaf58a3a03df.xml, display.dd_deferred_agp_aware_data
req.header: d3dhal.h
req.include-header: D3dhal.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DD_DEFERRED_AGP_AWARE_DATA
f1_keywords:
 - _DD_DEFERRED_AGP_AWARE_DATA
 - d3dhal/_DD_DEFERRED_AGP_AWARE_DATA
 - DD_DEFERRED_AGP_AWARE_DATA
 - d3dhal/DD_DEFERRED_AGP_AWARE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dhal.h
api_name:
 - _DD_DEFERRED_AGP_AWARE_DATA
 - DD_DEFERRED_AGP_AWARE_DATA
---

# _DD_DEFERRED_AGP_AWARE_DATA structure


## -description

   DirectX 8.0 and later versions and NT-based operating systems only.
   

DD_DEFERRED_AGP_AWARE_DATA is the data structure pointed to by the <b>lpvData</b> field of <a href="/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverinfodata">DD_GETDRIVERINFODATA</a> for D3DGDI2_TYPE_DEFERRED_AGP_AWARE notifications.

## -struct-fields

### -field gdi2

Specifies a <a href="/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_dd_getdriverinfo2data">DD_GETDRIVERINFO2DATA</a> structure that contains the <b>GetDriverInfo2</b> data.

## -remarks

Whenever a display device is created, the driver receives a <b>GetDriverInfo2</b> call with D3DGDI2_TYPE_DEFERRED_AGP_AWARE type and can determine if it should disable its other mechanisms that handle AGP memory and instead use the D3DGDI2_TYPE_FREE_DEFERRED_AGP and D3DGDI2_TYPE_DEFER_AGP_FREES notifications that the runtime subsequently sends.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_dd_getdriverinfo2data">DD_GETDRIVERINFO2DATA</a>



<a href="/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverinfodata">DD_GETDRIVERINFODATA</a>

