---
UID: NF:wudfusb.IWDFUsbTargetPipe.GetType
title: IWDFUsbTargetPipe::GetType (wudfusb.h)
description: The GetType method retrieves the type of a USB pipe.
old-location: wdf\iwdfusbtargetpipe_gettype.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["IWDFUsbTargetPipe::GetType"]
ms.keywords: GetType, GetType method, GetType method,IWDFUsbTargetPipe interface, IWDFUsbTargetPipe interface,GetType method, IWDFUsbTargetPipe.GetType, IWDFUsbTargetPipe::GetType, UMDFUSBref_792b0720-a0c3-45da-b5e8-7b2f3a0c3770.xml, umdf.iwdfusbtargetpipe_gettype, wdf.iwdfusbtargetpipe_gettype, wudfusb/IWDFUsbTargetPipe::GetType
req.header: wudfusb.h
req.include-header: Wudfusb.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
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
 - IWDFUsbTargetPipe::GetType
 - wudfusb/IWDFUsbTargetPipe::GetType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WUDFx.dll
api_name:
 - IWDFUsbTargetPipe::GetType
---

# IWDFUsbTargetPipe::GetType


## -description

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetType</b> method retrieves the type of a USB pipe.

## -returns

<b>GetType</b> returns a USBD_PIPE_TYPE value that identifies the type of the USB pipe.

## -remarks

The <b>GetType</b> method is provided for convenience because a UMDF driver can obtain the type of the USB pipe from the <b>PipeType</b> member of the <a href="/windows/win32/api/winusbio/ns-winusbio-winusb_pipe_information">WINUSB_PIPE_INFORMATION</a> structure that the driver retrieves when it calls the <a href="/windows-hardware/drivers/ddi/wudfusb/nf-wudfusb-iwdfusbtargetpipe-getinformation">IWDFUsbTargetPipe::GetInformation</a> method. 

For a code example of how to use the <b>GetType</b> method, see <a href="/windows-hardware/drivers/ddi/wudfusb/nf-wudfusb-iwdfusbinterface-getnumendpoints">IWDFUsbInterface::GetNumEndPoints</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/wudfusb/nn-wudfusb-iwdfusbtargetpipe">IWDFUsbTargetPipe</a>



<a href="/windows-hardware/drivers/ddi/wudfusb/nf-wudfusb-iwdfusbtargetpipe-getinformation">IWDFUsbTargetPipe::GetInformation</a>

