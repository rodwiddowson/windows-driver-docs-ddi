---
UID: NS:ntddcdrm._SUB_Q_CURRENT_POSITION
title: _SUB_Q_CURRENT_POSITION (ntddcdrm.h)
description: The SUB_Q_CURRENT_POSITION structure contains position information and is used in conjunction with SUB_Q_CHANNEL_DATA.
old-location: storage\sub_q_current_position.htm
tech.root: storage
ms.date: 01/08/2020
keywords: ["SUB_Q_CURRENT_POSITION structure"]
ms.keywords: "*PSUB_Q_CURRENT_POSITION, PSUB_Q_CURRENT_POSITION, PSUB_Q_CURRENT_POSITION structure pointer [Storage Devices], SUB_Q_CURRENT_POSITION, SUB_Q_CURRENT_POSITION structure [Storage Devices], _SUB_Q_CURRENT_POSITION, ntddcdrm/PSUB_Q_CURRENT_POSITION, ntddcdrm/SUB_Q_CURRENT_POSITION, storage.sub_q_current_position, structs-CD-ROM_f9833ad0-bb9c-418e-8e98-2c2f790a0e7e.xml"
req.header: ntddcdrm.h
req.include-header: Ntddcdrm.h
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
req.typenames: SUB_Q_CURRENT_POSITION, *PSUB_Q_CURRENT_POSITION
f1_keywords:
 - _SUB_Q_CURRENT_POSITION
 - ntddcdrm/_SUB_Q_CURRENT_POSITION
 - PSUB_Q_CURRENT_POSITION
 - ntddcdrm/PSUB_Q_CURRENT_POSITION
 - SUB_Q_CURRENT_POSITION
 - ntddcdrm/SUB_Q_CURRENT_POSITION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddcdrm.h
api_name:
 - SUB_Q_CURRENT_POSITION
---

# _SUB_Q_CURRENT_POSITION structure


## -description

The SUB_Q_CURRENT_POSITION structure contains position information and is used in conjunction with [SUB_Q_CHANNEL_DATA](./ns-ntddcdrm-_sub_q_channel_data.md).

## -struct-fields

### -field Header

Indicates, among other things, the length of the Q subchannel data that was retrieved. See [SUB_Q_HEADER](./ns-ntddcdrm-_sub_q_header.md) for more details.

### -field FormatCode

Should have a value of IOCTL_CDROM_CURRENT_POSITION.

### -field Control

Defines various types of information within the table of contents lead-in area. For more information about the permissible values for this member, see specification *T10/1363-D*, by National Committee for Information Technology Standards (NCITS).

### -field ADR

Indicates the type of information encoded in the Q subchannel of the block. For information about the permissible values for this member, see specification *T10/1363-D*, by National Committee for Information Technology Standards (NCITS).

### -field TrackNumber

Contains the current track number.

### -field IndexNumber

Contains the current index number.

### -field AbsoluteAddress

Gives the current location relative to the logical beginning of the media. The bytes in this array are arranged in big-endian order. **AbsoluteAddress**[0] contains the most significant byte, and **AbsoluteAddress**[3] contains the least significant byte.

### -field TrackRelativeAddress

Gives the current location relative to the logical beginning of the current track. The bytes in this array are arranged in big-endian order. **TrackRelativeAddress**[0] contains the most significant byte, and **TrackRelativeAddress**[3] contains the least significant byte.

## -see-also

[CDROM_SUB_Q_DATA_FORMAT](./ns-ntddcdrm-_cdrom_sub_q_data_format.md)

[IOCTL_CDROM_READ_Q_CHANNEL](./ni-ntddcdrm-ioctl_cdrom_read_q_channel.md)

[SUB_Q_CHANNEL_DATA](./ns-ntddcdrm-_sub_q_channel_data.md)

[SUB_Q_HEADER](./ns-ntddcdrm-_sub_q_header.md)
