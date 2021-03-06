---
UID: NF:nfccx.NfcCxUnregisterSequenceHandler
title: NfcCxUnregisterSequenceHandler function (nfccx.h)
description: Called by the client driver during device shutdown to unregister for the previously registered sequence handler callback.
old-location: nfpdrivers\_nfccxunregistersequencehandler.htm
tech.root: nfpdrivers
ms.date: 02/15/2018
keywords: ["NfcCxUnregisterSequenceHandler function"]
ms.keywords: NfcCxUnregisterSequenceHandler, NfcCxUnregisterSequenceHandler method [Near-Field Proximity Drivers], nfccx/NfcCxUnregisterSequenceHandler, nfpdrivers._nfccxunregistersequencehandler
req.header: nfccx.h
req.include-header: Ncidef.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Nfccxstub.lib
req.dll: NfcCx.dll
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - NfcCxUnregisterSequenceHandler
 - nfccx/NfcCxUnregisterSequenceHandler
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NfcCx.dll
api_name:
 - NfcCxUnregisterSequenceHandler
---

# NfcCxUnregisterSequenceHandler function


## -description

Called by the client driver during device shutdown to unregister for the previously registered sequence handler callback.

## -parameters

### -param Device

A handle to a framework device object.

### -param Sequence

An <a href="/windows-hardware/drivers/ddi/nfccx/ne-nfccx-_nfc_cx_sequence">NFC_CX_SEQUENCE</a>-typed enumerator.

## -returns

If the operation succeeds, the function returns STATUS_SUCCESS.

## -see-also

<a href="/windows-hardware/drivers/nfc/nfc-class-extension-">NFC class extension design guide</a>



<a href="/windows-hardware/drivers/nfc/">Near field communication (NFC) design guide</a>
