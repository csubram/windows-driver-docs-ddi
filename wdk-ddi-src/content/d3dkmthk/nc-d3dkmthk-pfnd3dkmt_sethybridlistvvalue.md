---
UID: NC:d3dkmthk.PFND3DKMT_SETHYBRIDLISTVVALUE
title: PFND3DKMT_SETHYBRIDLISTVVALUE (d3dkmthk.h)
description: The PFND3DKMT_SETHYBRIDLISTVVALUE callback function sets the hybrid list value.
ms.date: 10/19/2018
keywords: ["PFND3DKMT_SETHYBRIDLISTVVALUE callback function"]
req.header: d3dkmthk.h
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
ms.custom: RS5
tech.root: display
f1_keywords:
 - PFND3DKMT_SETHYBRIDLISTVVALUE
 - d3dkmthk/PFND3DKMT_SETHYBRIDLISTVVALUE
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dkmthk.h
api_name:
 - PFND3DKMT_SETHYBRIDLISTVVALUE
dev_langs:
 - c++
---

# PFND3DKMT_SETHYBRIDLISTVVALUE callback function


## -description

The PFND3DKMT_SETHYBRIDLISTVVALUE callback function sets the hybrid list value.

## -parameters

### -param Arg1

Pointer to a [D3DKMT_HYBRID_LIST](ns-d3dkmthk-_d3dkmt_hybrid_list.md) structure.

## -returns

Returns NTSTATUS.

## -prototype

```cpp
//Declaration

PFND3DKMT_SETHYBRIDLISTVVALUE Pfnd3dkmtSethybridlistvvalue; 

// Definition

NTSTATUS Pfnd3dkmtSethybridlistvvalue 
(
	D3DKMT_HYBRID_LIST *
)
{...}

```

## -remarks

## -see-also

