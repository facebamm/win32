﻿---
Description: 'Specifies the FOURCC that identifies the encoder you want to use.'
ms.assetid: 'c03da576-cb58-4686-af6f-9575520c759c'
title: 'MFPKEY\_FOURCC Property'
---

# MFPKEY\_FOURCC Property

Specifies the FOURCC that identifies the encoder you want to use.

## Constant for IPropertyBag

g\_wszWMVCFOURCC

## Data Type

VT\_I4 (FOURCC value)

## Remarks

You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:

-   [MFPKEY\_BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

You should use [**IWMCodecProps::GetCodecProp**](iwmcodecpropsgetcodecprop.md) to retrieve the values of the FOURCC-dependent properties listed previously. When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Properties](media-foundation-properties.md)
</dt> </dl>

 

 



