---
UID: NF:wiautil.WIAS_LTRACE
title: WIAS_LTRACE macro (wiautil.h)
description: The WIAS_LTRACE macro is obsolete for Windows Vista and later. It is recommended that the WIAS_TRACE macro be used instead.The WIAS_LTRACE macro writes a diagnostic WIA_TRACE message to the log file.
old-location: image\wias_ltrace.htm
tech.root: image
ms.date: 05/03/2018
keywords: ["WIAS_LTRACE macro"]
ms.keywords: IWiaLog_bb7ae826-5b43-47c1-bf94-bd491d8b91a7.xml, WIAS_LTRACE, WIAS_LTRACE macro [Imaging Devices], image.wias_ltrace, wiamdef/WIAS_LTRACE
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Obsolete. Use WIAS_TRACE instead.
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
 - WIAS_LTRACE
 - wiautil/WIAS_LTRACE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wiamdef.h
api_name:
 - WIAS_LTRACE
---

# WIAS_LTRACE macro (wiautil.h)


## -description

The WIAS_LTRACE macro is obsolete. It is recommended that the [WIAS_TRACE](../wiamdef/nf-wiamdef-wias_trace.md) macro be used instead.

The WIAS_LTRACE macro writes a diagnostic WIA_TRACE message to the log file.

## -parameters

### -param x

### -param y

### -param z

### -param params

- **DetailLevel** - Specifies the diagnostic detail level of the message. This parameter can be one of the following values.

    | Value | Description |
    | --- | --- |
    | WIALOG_LEVEL1 | Logs entry and exit points for all WIA methods and functions. |
    | WIALOG_LEVEL2 | Logs additional details for WIALOG_LEVEL1. |
    | WIALOG_LEVEL3 | Logs entry and exit points for all WIA methods and functions and additional vendor-supplied functions. |
    | WIALOG_LEVEL4 | Logs additional details for WIALOG_LEVEL3. |
    | WIALOG_LEVELXXX | User-defined log levels. |

- **ResourceID** - Specifies the resource ID. This value should be set to WIALOG_NO_RESOURCE_ID.

- **format_string** - Specifies a variable argument list, which starts with an ANSI format string describing the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".

- **pIWiaLog** - Pointer to an [IWiaLog Interface](../wia_lh/nn-wia_lh-iwialog.md).

## -remarks

The following is an example of how the macro can be used:

```cpp
WIAS_LTRACE(g_pIWiaLog, WIALOG_NO_RESOURCE_ID, WIALOG_LEVEL2,
  ("MyClass::MyMethod, This is my text and my lValue = %d", lValue));
```

Use of the WIAS_LTRACE macro is not recommended because it does not record its output to the *Wiatrace.log* diagnostic log file. It is recommended that the [WIAS_TRACE](../wiamdef/nf-wiamdef-wias_trace.md) macro be used instead.

## -see-also

[WIAS_LERROR](../wiamdef/nf-wiamdef-wias_lerror.md)

[WIAS_LHRESULT](../wiamdef/nf-wiamdef-wias_lhresult.md)

[WIAS_LWARNING](../wiamdef/nf-wiamdef-wias_lwarning.md)

[WIAS_TRACE](../wiamdef/nf-wiamdef-wias_trace.md)
