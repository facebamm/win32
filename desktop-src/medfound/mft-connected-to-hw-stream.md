﻿---
Description: 'Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.'
ms.assetid: '9166c43f-d2ae-4dc7-84e9-02146b67efe2'
title: 'MFT\_CONNECTED\_TO\_HW\_STREAM attribute'
---

# MFT\_CONNECTED\_TO\_HW\_STREAM attribute

Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.

## Data type

**UINT32**

## Get/set

To get this attribute, call [**IMFAttributes::GetUINT32**](imfattributes-getuint32.md).

To set this attribute, call [**IMFAttributes::SetUINT32**](imfattributes-setuint32.md).

## Remarks

Applications typically do not use this attribute.

This attribute is used with hardware-based MFTs. When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:

-   The output stream of the upstream MFT
-   The input stream of the downstream MFT

To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](imftransform-getoutputstreamattributes.md) on the upstream MFT. To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](imftransform-getinputstreamattributes.md) on the downstream MFT.

The GUID constant for this attribute is exported from mfuuid.lib.

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps \| UWP apps\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps \| UWP apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## See also

<dl> <dt>

[Alphabetical List of Media Foundation Attributes](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware MFTs](hardware-mfts.md)
</dt> <dt>

[Transform Attributes](transform-attributes.md)
</dt> </dl>

 

 



