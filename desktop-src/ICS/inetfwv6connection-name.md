---
title: INetFwV6Connection Name property
description: Specifies the display name of the connection. For example, the FriendlyName member of the IP\_ADAPTER\_ADDRESSES structure for this connection.
ms.assetid: '348172c6-bdba-486b-bf1e-ff449a4ae531'
keywords: ["Name property ICS/ICF", "Name property ICS/ICF , INetFwV6Connection interface", "INetFwV6Connection interface ICS/ICF , Name property"]
topic_type:
- apiref
api_name:
- INetFwV6Connection.Name
- INetFwV6Connection.get_Name
api_location:
- Netfwv6.dll
api_type:
- COM
---

# INetFwV6Connection::Name property

\[The IPv6 Internet Connection Firewall is available for use in the operating systems specified in the Requirements section. Instead, use the [Windows Firewall API](windows-firewall-start-page.md).\]

Specifies the display name of the connection. For example, the **FriendlyName** member of the [IP\_ADAPTER\_ADDRESSES](https://msdn.microsoft.com/library/windows/desktop/aa366058) structure for this connection.

This property is read-only.

## Syntax


```C++
HRESULT get_Name(
  [out]�BSTR *pbstrName
);
```



## Property value

Display name of the connection.

## Error codes

If the method succeeds the return value is S\_OK.

If the method fails, the return value is one of the following error codes.



| Name                                                                                      | Meaning                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>E\_ABORT</dt> </dl>       | The operation was aborted.<br/>                         |
| <dl> <dt>E\_FAIL</dt> </dl>        | An unspecified error occurred.<br/>                     |
| <dl> <dt>E\_INVALIDARG</dt> </dl>  | The parameter is invalid.<br/>                          |
| <dl> <dt>E\_NOINTERFACE</dt> </dl> | A specified interface is not supported.<br/>            |
| <dl> <dt>E\_NOTIMPL</dt> </dl>     | A specified method is not implemented.<br/>             |
| <dl> <dt>E\_OUTOFMEMORY</dt> </dl> | The method was unable to allocate required memory.<br/> |
| <dl> <dt>E\_POINTER</dt> </dl>     | A pointer passed as a parameter is not valid.<br/>      |
| <dl> <dt>E\_UNEXPECTED</dt> </dl>  | The method failed for unknown reasons.<br/>             |



## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP with SP1 \[desktop apps only\]<br/>                                   |
| Minimum supported server<br/> | None supported<br/>                                                              |
| End of client support<br/>    | Windows�XP with SP1<br/>                                                         |
| Redistributable<br/>          | Advanced Networking Pack for Windows�XP<br/>                                     |
| Header<br/>                   | <dl> <dt>Netfwv6.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Netfwv6.dll</dt> </dl> |



## See also

<dl> <dt>

[INetFwV6Connection](https://msdn.microsoft.com/library/windows/desktop/aa365570)
</dt> <dt>

[**INetFwV6Connection**](inetfwv6connection.md)
</dt> </dl>

�

�




