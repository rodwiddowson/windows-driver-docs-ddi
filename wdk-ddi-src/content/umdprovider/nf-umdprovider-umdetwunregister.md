---
UID: NF:umdprovider.UMDEtwUnregister
title: UMDEtwUnregister function (umdprovider.h)
description: Unregisters the event trace provider. Call this function before the user-mode driver is unloaded. After this function is called, the driver should not make any other calls to log events.
old-location: display\umdetwunregister.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["UMDEtwUnregister function"]
ms.keywords: UMDEtwUnregister, UMDEtwUnregister function [Display Devices], display.umdetwunregister, umdprovider/UMDEtwUnregister
req.header: umdprovider.h
req.include-header: Umdprovider.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - UMDEtwUnregister
 - umdprovider/UMDEtwUnregister
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - umdprovider.h
api_name:
 - UMDEtwUnregister
---

# UMDEtwUnregister function


## -description

Unregisters the event trace provider. Call this function before the user-mode driver is unloaded. After this function is called, the driver should not make any other calls to log events.

## -remarks

<b>UMDEtwUnregister</b> is defined inline in Umdprovider.h as:

```cpp
// Registration handle, returned by EventRegister and passed to EventUnregister
__declspec(selectany) REGHANDLE RegHandle = NULL;

FORCEINLINE void UMDEtwUnregister()
{
    EventUnregister(RegHandle);
}
```

The <a href="/windows/win32/api/evntprov/nf-evntprov-eventunregister">EventUnregister</a> function is  described in the <a href="/windows/desktop/Events/windows-events">Windows Events</a> documentation.

## -see-also

<a href="/windows-hardware/drivers/ddi/umdprovider/nf-umdprovider-umdetwregister">UMDEtwRegister</a>
