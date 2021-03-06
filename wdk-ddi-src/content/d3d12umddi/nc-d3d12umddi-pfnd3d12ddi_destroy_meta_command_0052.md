---
UID: NC:d3d12umddi.PFND3D12DDI_DESTROY_META_COMMAND_0052
title: PFND3D12DDI_DESTROY_META_COMMAND_0052 (d3d12umddi.h)
description: Destroys a meta-command.
ms.date: 10/19/2018
keywords: ["PFND3D12DDI_DESTROY_META_COMMAND_0052 callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
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
tech.root: display
ms.custom: RS5
f1_keywords:
 - PFND3D12DDI_DESTROY_META_COMMAND_0052
 - d3d12umddi/PFND3D12DDI_DESTROY_META_COMMAND_0052
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_DESTROY_META_COMMAND_0052
dev_langs:
 - c++
---

# PFND3D12DDI_DESTROY_META_COMMAND_0052 callback function


## -description

Destroys a meta-command.

## -parameters

### -param Arg1

A handle to the display device (graphics context).

### -param Arg2

Handle to a meta-command.

## -prototype

```cpp
//Declaration

PFND3D12DDI_DESTROY_META_COMMAND_0052 Pfnd3d12ddiDestroyMetaCommand0052; 

// Definition

VOID Pfnd3d12ddiDestroyMetaCommand0052 
(
	D3D12DDI_HDEVICE Arg1
	D3D12DDI_HMETACOMMAND_0052 Arg2
)
{...}

```

## -remarks

## -see-also

