---
UID: NS:iddcx.IDDCX_MOVEREGION
title: IDDCX_MOVEREGION (iddcx.h)
description: Gives information about the current move region.
old-location: display\iddcx_moveregion.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["IDDCX_MOVEREGION structure"]
ms.keywords: IDDCX_MOVEREGION, IDDCX_MOVEREGION structure [Display Devices], display.iddcx_moveregion, iddcx/IDDCX_MOVEREGION
req.header: iddcx.h
req.include-header: 
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
req.typenames: 
f1_keywords:
 - IDDCX_MOVEREGION
 - iddcx/IDDCX_MOVEREGION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iddcx.h
api_name:
 - IDDCX_MOVEREGION
---

# IDDCX_MOVEREGION structure


## -description

                 Gives information about the current move region.

## -struct-fields

### -field Size

                     Total size of the structure.

### -field SourcePoint

                     The location within the surface of the top left of the source rect. The source rect size is the same as the
    destination rect size.

### -field DestRect

                     Defines the destination rect of the move.

