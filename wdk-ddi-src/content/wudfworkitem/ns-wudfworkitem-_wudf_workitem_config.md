---
UID: NS:wudfworkitem._WUDF_WORKITEM_CONFIG
title: _WUDF_WORKITEM_CONFIG (wudfworkitem.h)
description: The WUDF_WORKITEM_CONFIG structure contains information that is associated with a work item.
old-location: wdf\wudf_workitem_config.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["WUDF_WORKITEM_CONFIG structure"]
ms.keywords: "*PWUDF_WORKITEM_CONFIG, PWUDF_WORKITEM_CONFIG, PWUDF_WORKITEM_CONFIG structure pointer, WUDF_WORKITEM_CONFIG, WUDF_WORKITEM_CONFIG structure, _WUDF_WORKITEM_CONFIG, umdf.wudf_workitem_config, wdf.wudf_workitem_config, wudfworkitem/PWUDF_WORKITEM_CONFIG, wudfworkitem/WUDF_WORKITEM_CONFIG"
req.header: wudfworkitem.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WUDF_WORKITEM_CONFIG, *PWUDF_WORKITEM_CONFIG
f1_keywords:
 - _WUDF_WORKITEM_CONFIG
 - wudfworkitem/_WUDF_WORKITEM_CONFIG
 - PWUDF_WORKITEM_CONFIG
 - wudfworkitem/PWUDF_WORKITEM_CONFIG
 - WUDF_WORKITEM_CONFIG
 - wudfworkitem/WUDF_WORKITEM_CONFIG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wudfworkitem.h
api_name:
 - _WUDF_WORKITEM_CONFIG
 - PWUDF_WORKITEM_CONFIG
 - WUDF_WORKITEM_CONFIG
---

# _WUDF_WORKITEM_CONFIG structure


## -description

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The 
   
  <b>WUDF_WORKITEM_CONFIG</b> structure contains information that is associated with a work item.

## -struct-fields

### -field Size

The size, in bytes, of this structure.

### -field OnWorkItemFunc

The address of an <a href="/windows-hardware/drivers/ddi/wudfworkitem/nc-wudfworkitem-wudf_workitem_function">OnWorkItem</a> callback function.

### -field AutomaticSerialization

A Boolean value that, if TRUE, indicates that the framework will synchronize execution of the <a href="/windows-hardware/drivers/ddi/wudfworkitem/nc-wudfworkitem-wudf_workitem_function">OnWorkItem</a> callback function with callback functions from other objects that are underneath the work-item object's parent object. If FALSE, the framework does not synchronize execution of the <i>OnWorkItem</i> callback function.

## -remarks

Your driver must initialize the <b>WUDF_WORKITEM_CONFIG</b> structure by calling <a href="/windows-hardware/drivers/ddi/wudfworkitem/nf-wudfworkitem-wudf_workitem_config_init">WUDF_WORKITEM_CONFIG_INIT</a>. Your driver can then pass the structure to the <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice3-createworkitem">IWDFDevice3::CreateWorkItem</a> method as an input parameter.

Setting the <b>AutomaticSerialization</b> member of <b>WUDF_WORKITEM_CONFIG</b> to TRUE has no effect if the driver did not enable automatic callback synchronization by calling <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdeviceinitialize-setlockingconstraint">IWDFDeviceInitialize::SetLockingConstraint</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice3-createworkitem">IWDFDevice3::CreateWorkItem</a>



<a href="/windows-hardware/drivers/ddi/wudfworkitem/nc-wudfworkitem-wudf_workitem_function">OnWorkItem</a>



<a href="/windows-hardware/drivers/ddi/wudfworkitem/nf-wudfworkitem-wudf_workitem_config_init">WUDF_WORKITEM_CONFIG_INIT</a>

