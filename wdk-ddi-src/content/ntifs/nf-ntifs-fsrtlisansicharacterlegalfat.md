---
UID: NF:ntifs.FsRtlIsAnsiCharacterLegalFat
title: FsRtlIsAnsiCharacterLegalFat macro (ntifs.h)
description: The FsRtlIsAnsiCharacterLegalFat macro determines whether an ANSI character is legal for FAT file names.
old-location: ifsk\fsrtlisansicharacterlegalfat.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FsRtlIsAnsiCharacterLegalFat macro"]
ms.keywords: FsRtlIsAnsiCharacterLegalFat, FsRtlIsAnsiCharacterLegalFat function [Installable File System Drivers], fsrtlref_9d13203c-5fc4-4f4f-9372-09459f053bbc.xml, ifsk.fsrtlisansicharacterlegalfat, ntifs/FsRtlIsAnsiCharacterLegalFat
req.header: ntifs.h
req.include-header: Ntifs.h
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
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - FsRtlIsAnsiCharacterLegalFat
 - ntifs/FsRtlIsAnsiCharacterLegalFat
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - FsRtlIsAnsiCharacterLegalFat
---

# FsRtlIsAnsiCharacterLegalFat macro


## -description

The <b>FsRtlIsAnsiCharacterLegalFat</b> macro determines whether an ANSI character is legal for FAT file names.

## -parameters

### -param C

<p>Pointer to the character to be tested.</p>

### -param WILD_OK

<p>Set to <b>TRUE</b> if wildcard characters are to be considered legal, <b>FALSE</b> otherwise.</p>

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlisansicharacterlegal">FsRtlIsAnsiCharacterLegal</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlisansicharacterlegalhpfs">FsRtlIsAnsiCharacterLegalHpfs</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlisansicharacterlegalntfs">FsRtlIsAnsiCharacterLegalNtfs</a>
