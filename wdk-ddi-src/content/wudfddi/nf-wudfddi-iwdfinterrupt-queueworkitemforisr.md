---
UID: NF:wudfddi.IWDFInterrupt.QueueWorkItemForIsr
title: IWDFInterrupt::QueueWorkItemForIsr (wudfddi.h)
description: The QueueWorkItemForIsr method queues a work item to process interrupt-related work outside of the interrupt service routine.
old-location: wdf\iwdfinterrupt_queueworkitemforisr.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["IWDFInterrupt::QueueWorkItemForIsr"]
ms.keywords: IWDFInterrupt interface,QueueWorkItemForIsr method, IWDFInterrupt.QueueWorkItemForIsr, IWDFInterrupt::QueueWorkItemForIsr, QueueWorkItemForIsr, QueueWorkItemForIsr method, QueueWorkItemForIsr method,IWDFInterrupt interface, umdf.iwdfinterrupt_queueworkitemforisr, wdf.iwdfinterrupt_queueworkitemforisr, wudfddi/IWDFInterrupt::QueueWorkItemForIsr
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
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
req.dll: WUDFx.dll
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDFInterrupt::QueueWorkItemForIsr
 - wudfddi/IWDFInterrupt::QueueWorkItemForIsr
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WUDFx.dll
api_name:
 - IWDFInterrupt::QueueWorkItemForIsr
---

# IWDFInterrupt::QueueWorkItemForIsr


## -description

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>QueueWorkItemForIsr</b> method queues a work item to process interrupt-related work outside of the interrupt service routine.

## -returns

The method returns TRUE if a work item was successfully queued. If a work item is already in the queue, the method returns FALSE.

## -remarks

The driver provides a pointer to its <a href="/windows-hardware/drivers/ddi/wudfinterrupt/nc-wudfinterrupt-wudf_interrupt_workitem">OnInterruptWorkItem</a> callback function when it calls  <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice3-createinterrupt">IWDFDevice3::CreateInterrupt</a> to create the interrupt object.

For more information about handling interrupts in UMDF drivers, see <a href="/windows-hardware/drivers/wdf/accessing-hardware-and-handling-interrupts">Accessing Hardware and Handling Interrupts</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice3-createworkitem">IWDFDevice3::CreateWorkItem</a>



<a href="/windows-hardware/drivers/ddi/wudfddi/nn-wudfddi-iwdfinterrupt">IWDFInterrupt</a>



<a href="/windows-hardware/drivers/ddi/wudfinterrupt/nc-wudfinterrupt-wudf_interrupt_workitem">OnInterruptWorkItem</a>

