---
description: "Learn more about: BizTalkServiceInstance Class"
title: BizTalkServiceInstance Class
TOCTitle: BizTalkServiceInstance Class
ms:assetid: 5771903f-6eda-4ebf-b68b-5c81800ec9e5
ms:mtpsurl: https://msdn.microsoft.com/library/Bb727883(v=BTS.80)
ms:contentKeyID: 51528171
ms.date: 08/30/2017
mtps_version: v=BTS.80
---

# BizTalkServiceInstance Class

 

The **BizTalkServiceInstance** class implements the service contracts that the WCF adapters use to receive incoming messages. The WCF adapters create a separate **ServiceHost** and singleton service object of this class for each receive location to handle client requests for the lifetime of the BizTalk Host instance running WCF receive locations. The service object uses multiple threads to process messages concurrently unless the WCF-NetMsmq receive locations are used with the **Ordered processing** property being selected.


> [!WARNING]
> <P>This topic is provided for information only. You can use this information to interpret the instances that WCF performance counters create for the WCF adapters and the auto-generated metadata for the WCF adapters. Do not rely on this information when you create applications.</P>



## Interface Declaration

```C#
[ServiceBehavior(  
     InstanceContextMode = InstanceContextMode.Single,  
     ConcurrencyMode = ConcurrencyMode.Multiple  
     // NOTE: Some of these properties are configured at runtime in BtsServiceHost  
        )]  
internal sealed class BizTalkServiceInstance :  
     ITwoWayAsync,  
     ITwoWayAsyncVoid,  
     IOneWayAsync,  
     IOneWayAsyncTxn,  
     ITwoWayAsyncVoidTxn  
```

