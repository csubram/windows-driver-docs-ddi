---
UID: NF:dbgmodel.IKeyStore.ClearKeys
title: IKeyStore::ClearKeys (dbgmodel.h)
description: The ClearKeys method is analogous to the ClearKeys method on IModelObject.
ms.date: 08/13/2018
keywords: ["IKeyStore::ClearKeys"]
ms.keywords: IKeyStore::ClearKeys, ClearKeys, IKeyStore.ClearKeys, IKeyStore::ClearKeys, IKeyStore.ClearKeys
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - IKeyStore::ClearKeys
 - dbgmodel/IKeyStore::ClearKeys
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IKeyStore::ClearKeys
---

# IKeyStore::ClearKeys


## -description

The ClearKeys method is analogous to the ClearKeys method on [IModelObject](nn-dbgmodel-imodelobject.md). It will remove every key from the given metadata store. This method has no effect on any parent store.

## -returns

This method returns HRESULT that indicates success or failure.

## -remarks

**Code Sample**

```cpp
ComPtr<IKeyStore> spMetadata; /* get a metadata store */

if (SUCCEEDED(spMetadata->ClearKeys()))
{
    // The metadata store is now empty.  A parent store may still have keys 
    // and GetKey[Value] may find those keys and values.
}
```

## -see-also

[IKeyStore interface](nn-dbgmodel-ikeystore.md)

