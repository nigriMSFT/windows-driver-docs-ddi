---
UID: NS:sidebandaudio.__unnamed_union_0
title: SIDEBANDAUDIO_IO_PARAM_HEADER (sidebandaudio.h)
description: Describes the size and type of parameter.
ms.date: 10/19/2021
keywords: ["SIDEBANDAUDIO_IO_PARAM_HEADER structure"]
ms.keywords: SIDEBANDAUDIO_IO_PARAM_HEADER, SIDEBANDAUDIO_IO_PARAM_HEADER, *PSIDEBANDAUDIO_IO_PARAM_HEADER,
req.header: sidebandaudio.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: SIDEBANDAUDIO_IO_PARAM_HEADER, *PSIDEBANDAUDIO_IO_PARAM_HEADER
targetos: Windows
tech.root: audio
ms.custom: RS5
f1_keywords:
 - PSIDEBANDAUDIO_IO_PARAM_HEADER
 - sidebandaudio/PSIDEBANDAUDIO_IO_PARAM_HEADER
 - SIDEBANDAUDIO_IO_PARAM_HEADER
 - sidebandaudio/SIDEBANDAUDIO_IO_PARAM_HEADER
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sidebandaudio.h
api_name:
 - PSIDEBANDAUDIO_IO_PARAM_HEADER
 - SIDEBANDAUDIO_IO_PARAM_HEADER
---

# SIDEBANDAUDIO_IO_PARAM_HEADER structure

## -description

Describes the size and type of the IO parameter.

## -struct-fields

### -field .ParamSet

Parameter Set - This could be Microsoft Standard set or IHV defined.

### -field .TypeId

Type of parameter.

### -field .Size

Size in bytes of Parameter. In case of IOCTL_SBAUD_GET_SIOPxxx Size will indicate size of any extra input parameter.

### -field Alignment

Allows for byte alignment.

## -remarks

Union fields described here.

#### ParamSet

Parameter Set - This could be Microsoft Standard set or IHV defined.

#### TypeId

Type of parameter.

#### Size

Size in bytes of Parameter. In case of IOCTL_SBAUD_GET_SIOPxxx Size will indicate size of any extra input parameter.

## -see-also

[sidebandaudio.h](index.md)

