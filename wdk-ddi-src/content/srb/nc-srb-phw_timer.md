---
UID: NC:srb.PHW_TIMER
title: PHW_TIMER (srb.h)
description: The PHW_TIMER routine prototype declares a SCSI miniport driver's timer routine.
old-location: storage\phw_timer.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["PHW_TIMER callback"]
ms.keywords: "(*PHW_TIMER), (*PHW_TIMER) callback function [Storage Devices], ide_minikr_55cc9012-04fa-434c-b2b9-d24bbd1d1404.xml, srb/(*PHW_TIMER), storage.phw_timer"
req.header: srb.h
req.include-header: Storport.h, Srb.h, Storport.h
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
req.irql: 
targetos: Windows
req.typenames: SPB_CONTROLLER_CONFIG, *PSPB_CONTROLLER_CONFIG
req.product: Windows 10 or later.
f1_keywords:
 - PHW_TIMER
 - srb/PHW_TIMER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - srb.h
api_name:
 - PHW_TIMER
---

# PHW_TIMER callback


## -description

The PHW_TIMER routine prototype declares a SCSI miniport driver's timer routine.

## -parameters

### -param DeviceExtension [in]


Pointer to the miniport driver's per-HBA storage area.

## -remarks

The SCSI miniport driver's timer routine, <a href="/previous-versions/windows/hardware/drivers/ff557327(v=vs.85)">HwScsiTimer</a>, is called after the interval specified when the miniport driver called <b>ScsiPortNotification</b> with the <b>RequestTimerCall</b><i>NotificationType</i> value.

Miniport drivers that work with the StorPort driver do not use this timer routine.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff557327(v=vs.85)">HwScsiTimer</a>

