---
UID: NC:storport.HW_TIMER
title: HW_TIMER (storport.h)
description: The HwStorTimer routine is called after the interval that is specified when the miniport driver called StorPortNotification with the RequestTimerCall NotificationType value.
old-location: storage\hwstortimer.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["HW_TIMER callback function"]
ms.keywords: HW_TIMER, HwStorTimer, HwStorTimer routine [Storage Devices], storage.hwstortimer, stormini_6127daf5-8672-4bf4-9241-b67bed14b8f8.xml, storport/HwStorTimer
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
 - HW_TIMER
 - storport/HW_TIMER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Storport.h
api_name:
 - HW_TIMER
---

# HW_TIMER callback function


## -description

The <b>HwStorTimer</b> routine is called after the interval that is specified when the miniport driver called <a href="/windows-hardware/drivers/ddi/storport/nf-storport-storportnotification">StorPortNotification</a> with the <b>RequestTimerCall</b><i> NotificationType</i> value.

## -parameters

### -param DeviceExtension

A pointer to the miniport driver's per HBA storage area.

## -remarks

The name <b>HwStorTimer</b> is only a placeholder. The actual prototype of this routine is defined in <i>Srb.h</i> as follows:


```
typedef
VOID
HW_TIMER (
  _In_ PVOID  DeviceExtension
  );
```

If the miniport opts into multi-channel support, the StartIo spin lock is still taken. However, if the miniport has requested multiple channel support via PERF_CONFIGURATION_DATA, the StartIo spin lock is not taken or checked before the call to <a href="/windows-hardware/drivers/ddi/storport/nc-storport-hw_startio">HwStorStartIo</a> in the miniport.  This means that the <i>HwStorStartIo</i> callback  is not synchronized with the callback to the <i>HwStorTimer</i> routine when multi-channel support is used.  The miniport must do this on its own by using a compiler interlocked intrinsic, for example using <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedcompareexchange">InterlockedCompareExchange</a>. 

A <b>HwStorTimer</b> routine is optional.


#### Examples

To define an <b>HwStorTimer</b> callback function, you must first provide a function declaration that identifies the type of callback function you’re defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="/windows-hardware/drivers/devtest/code-analysis-for-drivers">Code Analysis for Drivers</a>, <a href="/windows-hardware/drivers/devtest/static-driver-verifier">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it’s a requirement for writing drivers for the Windows operating system.

 For example, to define a <b>HwStorTimer</b> callback routine that is named <i>MyHwTimer</i>, use the <b>HW_TIMER</b> type as shown in this code example:


```
HW_TIMER MyHwTimer;
```

Then, implement your callback routine as follows:


```
_Use_decl_annotations_
VOID
MyHwTimer (
  _In_ PVOID  DeviceExtension
  );
  {
      ...
  }
```

The <b>HW_TIMER</b> function type is defined in the Storport.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>HW_TIMER</b> function type in the header file are used. For more information about the requirements for function declarations, see <a href="/windows-hardware/drivers/devtest/declaring-functions-by-using-function-role-types-for-storport-drivers">Declaring Functions Using Function Role Types for Storport Drivers</a>. For information about _Use_decl_annotations_, see <a href="/visualstudio/code-quality/annotating-function-behavior?view=vs-2015">Annotating Function Behavior</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/storport/nf-storport-storportnotification">StorPortNotification</a>

