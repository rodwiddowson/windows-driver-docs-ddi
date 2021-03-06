---
UID: NS:printoem.__unnamed_struct_0
title: IPPARAMS (printoem.h)
description: The IPPARAMS structure is used as an input parameter to a rendering plug-in's IPrintOemUni::ImageProcessing method.
old-location: print\ipparams.htm
tech.root: print
ms.date: 04/20/2018
keywords: ["IPPARAMS structure"]
ms.keywords: "*PIPPARAMS, IPPARAMS, IPPARAMS structure [Print Devices], PIPPARAMS, PIPPARAMS structure pointer [Print Devices], print.ipparams, print_unidrv-pscript_rendering_a002bc49-f3de-4147-bb33-8766672c8d0c.xml, printoem/IPPARAMS, printoem/PIPPARAMS"
req.header: printoem.h
req.include-header: Printoem.h
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
req.typenames: IPPARAMS, *PIPPARAMS
f1_keywords:
 - PIPPARAMS
 - printoem/PIPPARAMS
 - IPPARAMS
 - printoem/IPPARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - printoem.h
api_name:
 - IPPARAMS
---

# IPPARAMS structure


## -description

The IPPARAMS structure is used as an input parameter to a rendering plug-in's <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemuni-imageprocessing">IPrintOemUni::ImageProcessing</a> method.

## -struct-fields

### -field dwSize

Specifies the size, in bytes of the IPPARAMS structure. Supplied by Unidrv.

### -field ptOffset

Pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the banded image's offset from the upper left corner of the drawing area. Supplied by Unidrv.

### -field pHalftoneOption

Pointer to a string containing the name of the currently selected halftoning option. Supplied by Unidrv.

### -field bBanding

Specifies whether image banding is active. If <b>TRUE</b>, image banding is active. If <b>FALSE</b>, image banding is not active. Supplied by Unidrv.

### -field bBlankBand

Specifies whether a blank band was drawn in the source bitmap supplied to <a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemuni-imageprocessing">IPrintOemUni::ImageProcessing</a>. A value of <b>TRUE</b> indicates that nothing was drawn in the source bitmap supplied to <b>IPrintOemUni::ImageProcessing</b>. A <b>TRUE</b> value also indicates that data in the source bitmap is invalid and should not be processed. Supplied by Unidrv.

## -see-also

<a href="/windows-hardware/drivers/ddi/prcomoem/nf-prcomoem-iprintoemuni-imageprocessing">IPrintOemUni::ImageProcessing</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>
