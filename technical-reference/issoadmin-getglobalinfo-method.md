---
description: "Learn more about: ISSOAdmin.GetGlobalInfo Method"
title: ISSOAdmin.GetGlobalInfo Method
TOCTitle: ISSOAdmin.GetGlobalInfo Method
ms:assetid: 5699dbac-1467-4739-a940-9572e1b0415e
ms:mtpsurl: https://msdn.microsoft.com/library/Aa754780(v=BTS.80)
ms:contentKeyID: 51528165
ms.date: 08/30/2017
mtps_version: v=BTS.80
dev_langs:
- c++
- vb
---

# ISSOAdmin.GetGlobalInfo Method

 

The **GetGlobalInfo** method gets the global Enterprise Single Sign-On (SSO) configuration information from the Enterprise Single Sign-On server database.

## Syntax

``` c++
  
HRESULT GetGlobalInfo(  
LONG* plFlags,  
LONG* plAuditAppDeleteMax,  
LONG* plAuditMappingDeleteMax,  
LONG* plAuditNtpLookupMax,  
LONG* plAuditXpLookupMax,  
LONG* plTicketTimeout,  
LONG* plCredCacheTimeout,  
BSTR* pbstrSecretServer,  
BSTR* pbstrSSOAdminGroup,  
BSTR* pbstrAffiliateAppMgrGroup  
);  
```

``` vb
  
Function GetGlobalInfo(  
plFlags As Long,  
plAuditAppDeleteMax As Long,  
plAuditMappingDeleteMax As Long,  
plAuditNtpLookupMax As Long,  
plAuditXpLookupMax As Long,  
plTicketTimeout As Long,  
plCredCacheTimeout As Long,  
pbstrSecretServer As String,  
pbstrSSOAdminGroup As String  
)  
As String  
```

#### Parameters

plFlags  
\[out\] Pointer to a long integer that receives the global flags.

plFlags  
\[out\] Long that receives the global flags.

plAuditAppDeleteMax  
\[out\] Pointer to a long integer that receives the current size of the AuditAppDelete table.

plAuditAppDeleteMax  
\[out\] Long integer that receives the current size of the AuditAppDelete table.

plAuditMappingDeleteMax  
\[out\] Pointer to a long integer that receives the current size of the AuditMappingDelete table.

plAuditMappingDeleteMax  
\[out\] Long that receives the current size of the AuditMappingDelete table.

plAuditNtpLookupMax  
\[out\] Pointer to a long integer that receives the current size of the AuditNtpLookup table.

plAuditNtpLookupMax  
\[out\] Long that receives the current size of the AuditNtpLookup table.

plAuditXpLookupMax  
\[out\] Pointer to a long integer that receives the current size of the AuditXpLookup table.

plAuditXpLookupMax  
\[out\] Long that receives the current size of the AuditXpLookup table.

plTicketTimeout  
\[out\] Pointer to a long integer that receives the current ticket time-out value in minutes.

plTicketTimeout  
\[out\] Long that receives the current ticket time-out value in minutes.

plCredCacheTimeout  
\[out\] Pointer to a long integer that receives the current credential cache time-out value in minutes.

plCredCacheTimeout  
\[out\] Long that receives the current credential cache time-out value in minutes.

pbstrSecretServer  
\[out\] Pointer to a string that receives the current secret server computer name.

pbstrSecretServer  
\[out\] String that receives the current secret server computer name.

pbstrSSOAdminGroup  
\[out\] Pointer to a string that receives the current SSO server Administrator group name.

pbstrSSOAdminGroup  
\[out\] String that receives the current SSO server Administrator group name.

pbstrAffiliateAppMgrGroup  
\[out\] Pointer to a string that receives the current SSO server Affiliate Administrator group name.

## Return Value

This method returns an HRESULT indicating whether it completed successfully. For more details, see the Error Values section.

This method returns a String that receives the current SSO server Affiliate Administrator group name.

## Error Values

This method returns an HRESULT containing one of the values in the following table.

This method indicates errors by setting the Number property of the global **Err** object to one of the values in the following table.

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr class="even">
<td>E_ACCESSDENIED</td>
<td>Access is denied to the caller.</td>
</tr>
<tr class="odd">
<td>E_INVALIDARG</td>
<td>An invalid parameter was detected.</td>
</tr>
</tbody>
</table>


## Remarks

To access this method, you must be an SSO Administrator.

## Requirements

**Platforms:**  Windows

## See Also

[Programming with Enterprise Single Sign-On](https://msdn.microsoft.com/library/aa704508\(v=bts.80\))  
[ISSOAdmin Interface (COM)](issoadmin-interface-com.md)  
[ISSOAdmin Members](issoadmin-members.md)

