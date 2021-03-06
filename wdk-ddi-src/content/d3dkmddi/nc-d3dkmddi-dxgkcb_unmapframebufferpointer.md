---
UID: NC:d3dkmddi.DXGKCB_UNMAPFRAMEBUFFERPOINTER
title: DXGKCB_UNMAPFRAMEBUFFERPOINTER (d3dkmddi.h)
description: Implemented by the client driver to release the mapping that was set by DXGKCB_MAPFRAMEBUFFERPOINTER.
ms.date: 10/19/2018
keywords: ["DXGKCB_UNMAPFRAMEBUFFERPOINTER callback function"]
req.header: d3dkmddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: display
f1_keywords:
 - DXGKCB_UNMAPFRAMEBUFFERPOINTER
 - d3dkmddi/DXGKCB_UNMAPFRAMEBUFFERPOINTER
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3dkmddi.h
api_name:
 - DXGKCB_UNMAPFRAMEBUFFERPOINTER
product:
 - Windows
---

# DXGKCB_UNMAPFRAMEBUFFERPOINTER callback function


## -description

Implemented by the client driver to release the mapping that was set by [DXGKCB_MAPFRAMEBUFFERPOINTER](nc-d3dkmddi-dxgkcb_mapframebufferpointer.md).

## -parameters

### -param hAdapter

A handle to a display adapter. The driver provides this handle for the master/lead device in the LDA chain.

### -param pUnmapFrameBufferPointer

A pointer to the [DXGKARGCB_UNMAPFRAMEBUFFERPOINTER](ns-d3dkmddi-_dxgkargcb_unmapframebufferpointer.md) structure that contains a handle to the memory to be unmapped.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS Values error code.

## -prototype

```cpp
//Declaration

DXGKCB_UNMAPFRAMEBUFFERPOINTER DxgkcbUnmapframebufferpointer;

// Definition

NTSTATUS DxgkcbUnmapframebufferpointer
(
	IN_CONST_HANDLE hAdapter
	IN_CONST_PDXGKARGCB_UNMAPFRAMEBUFFERPOINTER pUnmapFrameBufferPointer
)
{...}

DXGKCB_UNMAPFRAMEBUFFERPOINTER


```

## -remarks

Register your implementation of this callback function by setting the appropriate member of DXGKARGCB_UNMAPFRAMEBUFFERPOINTER and then calling DxgkCbUnmapFrameBufferPointer.

## -see-also

