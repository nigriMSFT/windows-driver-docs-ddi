---
UID: NF:wia_lh.IWiaLog.Log
title: IWiaLog::Log (wia_lh.h)
description: The IWiaLog interface is obsolete and is no longer supported. Use the Diagnostic Log Macros instead.The IWiaLog::Log method writes a diagnostic log message to Wiaservc.log.
tech.root: image
ms.date: 04/19/2022
keywords: ["IWiaLog::Log"]
ms.keywords: IWiaLog interface [Imaging Devices],Log method, IWiaLog.Log, IWiaLog::Log, IWiaLog_e3605b5e-0494-46a7-85c1-3a0707a74764.xml, Log, Log method [Imaging Devices], Log method [Imaging Devices],IWiaLog interface, image.iwialog_log, wia_lh/IWiaLog::Log
req.header: wia_lh.h
req.include-header: Wia_lh.h
req.target-type: Desktop
req.target-min-winverclnt: Obsolete and is no longer supported. Instead, use the Diagnostic Log Macros.
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
 - IWiaLog::Log
 - wia_lh/IWiaLog::Log
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wia_lh.h
api_name:
 - IWiaLog::Log
---

## -description

The **IWiaLog** interface is obsolete and is no longer supported. Use the [Diagnostic Log Macros](../_image/index.md) instead.The **IWiaLog::Log** method writes a diagnostic log message to *Wiaservc.log*.

## -parameters

### -param lFlags [in]

Specifies the type of diagnostic message. This parameter can be WIA_WARNING, WIA_TRACE or WIA_ERROR.

### -param lResID [in]

Specifies the resource id. This parameter should be set to WIALOG_NO_RESOURCE_ID.

### -param lDetail

Specifies the diagnostic detail level of the message. This parameter can be one of the following values.

| Level | Description |
|--|--|
| WIALOG_LEVEL1 | Logs entry and exit points for all WIA methods and functions. |
| WIALOG_LEVEL2 | Logs additional details for WIALOG_LEVEL1. |
| WIALOG_LEVEL3 | Logs entry and exit points for all WIA methods and functions and additional vendor-supplied functions. |
| WIALOG_LEVEL4 | Logs additional details for WIALOG_LEVEL3. |
| WIALOG_LEVELXXX | User-defined log levels. |

### -param bstrText [in]

Specifies the error text. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".

## -returns

If the method succeeds, it returns S_OK.  If the method fails, it returns a standard COM error code.
