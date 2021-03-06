---
UID: NE:pointofservicecommontypes.DriverUnifiedPosHealthCheckLevel
title: DriverUnifiedPosHealthCheckLevel (pointofservicecommontypes.h)
description: This enumeration indicates the type of health check to be performed when CheckHealthAsync is called on a POS device.
old-location: pos\unifiedposhealthchecklevel.htm
tech.root: pos
ms.date: 02/23/2018
keywords: ["DriverUnifiedPosHealthCheckLevel enumeration"]
ms.keywords: DriverUnifiedPosHealthCheckLevel, DriverUnifiedPosHealthCheckLevel enumeration, External, Interactive, POSInternal, UnknownHealthCheckLevel, pointofservicecommontypes/DriverUnifiedPosHealthCheckLevel, pointofservicecommontypes/External, pointofservicecommontypes/Interactive, pointofservicecommontypes/POSInternal, pointofservicecommontypes/UnknownHealthCheckLevel, pos.unifiedposhealthchecklevel
req.header: pointofservicecommontypes.h
req.include-header: Pointofservicecommontypes.h
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
req.typenames: DriverUnifiedPosHealthCheckLevel
f1_keywords:
 - DriverUnifiedPosHealthCheckLevel
 - pointofservicecommontypes/DriverUnifiedPosHealthCheckLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - pointofservicecommontypes.h
api_name:
 - DriverUnifiedPosHealthCheckLevel
---

# DriverUnifiedPosHealthCheckLevel enumeration


## -description

This enumeration indicates the type of health check to be performed when CheckHealthAsync is called on a POS device.

## -enum-fields

### -field UnknownHealthCheckLevel

The type of health check is not known.

### -field POSInternal

Performs a health check without altering the device. The device is tested by internal tests as far as possible.

### -field External

Performs a more thorough test which may affect the device. For example, a printer may produce some output.

### -field Interactive

May display a dialog box that displays test options and results so that you can test the device interactively.

