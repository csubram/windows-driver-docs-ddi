---
UID: NF:dmusicks.IMiniportDMus.Service
title: IMiniportDMus::Service (dmusicks.h)
description: This method does not currently need to be implemented in the miniport driver. The Service method is currently unused.
old-location: audio\iminiportdmus_service.htm
tech.root: audio
ms.date: 05/08/2018
keywords: ["IMiniportDMus::Service"]
ms.keywords: IMiniportDMus interface [Audio Devices],Service method, IMiniportDMus.Service, IMiniportDMus::Service, Service, Service method [Audio Devices], Service method [Audio Devices],IMiniportDMus interface, audio.iminiportdmus_service, audmp-routines_0c872bc5-12b7-4e9d-b6ea-0da47cd41483.xml, dmusicks/IMiniportDMus::Service
req.header: dmusicks.h
req.include-header: Dmusicks.h
req.target-type: Desktop
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
req.typenames: 
f1_keywords:
 - IMiniportDMus::Service
 - dmusicks/IMiniportDMus::Service
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusicks.h
api_name:
 - IMiniportDMus::Service
---

# IMiniportDMus::Service


## -description

   This method does not currently need to be implemented in the miniport driver. The<code> Service</code> method is currently unused.

## -remarks

<code>Service</code> was intended to be called during a deferred procedure call (DPC) and was to be executed as the result of a call of the <a href="/windows-hardware/drivers/ddi/dmusicks/nf-dmusicks-iportdmus-notify">IPortDMus::Notify</a> method. Instead, the DMus port driver sends notification to the miniport driver's input stream by calling <a href="/windows-hardware/drivers/ddi/dmusicks/nf-dmusicks-imxf-putmessage">IMXF::PutMessage</a> with a <b>NULL</b> parameter value. Hence, <code>Service</code> is currently unused.

## -see-also

<a href="/windows-hardware/drivers/ddi/dmusicks/nf-dmusicks-imxf-putmessage">IMXF::PutMessage</a>



<a href="/windows-hardware/drivers/ddi/dmusicks/nn-dmusicks-iminiportdmus">IMiniportDMus</a>



<a href="/windows-hardware/drivers/ddi/dmusicks/nf-dmusicks-iportdmus-notify">IPortDMus::Notify</a>

