---
UID: NS:ucxusbdevice._USBDEVICE_ENABLE
title: _USBDEVICE_ENABLE (ucxusbdevice.h)
description: Contains parameters for a request to enable the specified device. This structure is passed by UCX in request parameters (Parameters.Others.Arg1) of a framework request object of the EVT_UCX_USBDEVICE_ENABLE callback function.
old-location: buses\_usbdevice_enable.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["USBDEVICE_ENABLE structure"]
ms.keywords: "*PUSBDEVICE_ENABLE, P_USBDEVICE_ENABLE, P_USBDEVICE_ENABLE structure pointer [Buses], USBDEVICE_ENABLE, USBDEVICE_ENABLE structure [Buses], _USBDEVICE_ENABLE, buses._usbdevice_enable, ucxusbdevice/P_USBDEVICE_ENABLE, ucxusbdevice/_USBDEVICE_ENABLE"
req.header: ucxusbdevice.h
req.include-header: Ucxclass.h
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
req.typenames: USBDEVICE_ENABLE, *PUSBDEVICE_ENABLE
f1_keywords:
 - _USBDEVICE_ENABLE
 - ucxusbdevice/_USBDEVICE_ENABLE
 - PUSBDEVICE_ENABLE
 - ucxusbdevice/PUSBDEVICE_ENABLE
 - USBDEVICE_ENABLE
 - ucxusbdevice/USBDEVICE_ENABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ucxusbdevice.h
api_name:
 - _USBDEVICE_ENABLE
 - PUSBDEVICE_ENABLE
 - USBDEVICE_ENABLE
---

# _USBDEVICE_ENABLE structure


## -description

Contains parameters for a request to enable the specified device. This structure is passed by UCX in request parameters (<b>Parameters.Others.Arg1</b>) of a framework request object of the <a href="/windows-hardware/drivers/ddi/ucxusbdevice/nc-ucxusbdevice-evt_ucx_usbdevice_enable">EVT_UCX_USBDEVICE_ENABLE</a> callback function.

## -struct-fields

### -field Header

A <a href="/windows-hardware/drivers/ddi/ucxusbdevice/ns-ucxusbdevice-_usbdevice_mgmt_header">USBDEVICE_MGMT_HEADER</a> structure that contains  the handle for the USB hub or device.

### -field DefaultEndpoint

The default endpoint for the USB hub or device to enable transfers for.

### -field FailureFlags

The errors, if any, that occurred when attempting to enable the hub or device for transfers.

## -see-also

<a href="/windows-hardware/drivers/ddi/ucxusbdevice/ns-ucxusbdevice-_usbdevice_disable">USBDEVICE_DISABLE</a>



<a href="/windows-hardware/drivers/ddi/wdfrequest/nf-wdfrequest-wdfrequestgetparameters">WdfRequestGetParameters</a>

