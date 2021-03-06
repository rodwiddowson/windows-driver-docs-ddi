---
UID: NS:iscsiop._RemoveConnectionFromSession_IN
title: _RemoveConnectionFromSession_IN (iscsiop.h)
description: The RemoveConnectionFromSession_IN structure holds the input data for the RemoveConnectionFromSession method, which is used to remove a connection from a session.
old-location: storage\removeconnectionfromsession_in.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["RemoveConnectionFromSession_IN structure"]
ms.keywords: "*PRemoveConnectionFromSession_IN, PRemoveConnectionFromSession_IN, PRemoveConnectionFromSession_IN structure pointer [Storage Devices], RemoveConnectionFromSession_IN, RemoveConnectionFromSession_IN structure [Storage Devices], _RemoveConnectionFromSession_IN, iscsiop/PRemoveConnectionFromSession_IN, iscsiop/RemoveConnectionFromSession_IN, storage.removeconnectionfromsession_in, structs-iSCSI_7dca8bd4-ebf8-4ccc-996a-852fabba5df3.xml"
req.header: iscsiop.h
req.include-header: Iscsiop.h
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
req.typenames: RemoveConnectionFromSession_IN, *PRemoveConnectionFromSession_IN
f1_keywords:
 - _RemoveConnectionFromSession_IN
 - iscsiop/_RemoveConnectionFromSession_IN
 - PRemoveConnectionFromSession_IN
 - iscsiop/PRemoveConnectionFromSession_IN
 - RemoveConnectionFromSession_IN
 - iscsiop/RemoveConnectionFromSession_IN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iscsiop.h
api_name:
 - RemoveConnectionFromSession_IN
---

# _RemoveConnectionFromSession_IN structure


## -description

The RemoveConnectionFromSession_IN structure holds the input data for the <a href="/windows-hardware/drivers/storage/removeconnectionfromsession">RemoveConnectionFromSession</a> method, which is used to remove a connection from a session.

## -struct-fields

### -field UniqueSessionId

A 64-bit integer that uniquely identifies the session. The <a href="/windows-hardware/drivers/storage/logintotarget">LoginToTarget</a> and <a href="/windows-hardware/drivers/storage/addconnectiontosession">AddConnectionToSession</a> methods both return this value in their <i>UniqueSessionId</i> parameter. Do not confuse this value with the values in the ISID and TSID members.

### -field UniqueConnectionId

A 64-bit integer that uniquely identifies the connection. Do not confuse this value with the connection ID (CID).

## -remarks

You must implement this class.

## -see-also

<a href="/windows-hardware/drivers/storage/addconnectiontosession">AddConnectionToSession</a>



<a href="/windows-hardware/drivers/storage/logintotarget">LoginToTarget</a>



<a href="/windows-hardware/drivers/storage/removeconnectionfromsession">RemoveConnectionFromSession</a>
