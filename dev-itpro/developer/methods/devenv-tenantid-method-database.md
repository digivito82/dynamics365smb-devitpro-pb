---
title: "TENANTID Method (Database)"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 070737cc-4fda-4fa9-84c6-976473d7e2e0
caps.latest.revision: 3
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# TENANTID Method (Database)
Gets the ID of the tenant that has started the current session.  
  
 Use this method when your code must be specific about which tenant database to access in a multitenant deployment. For example, if your code imports data into a cache, you can make a cache tenant-specific by using the tenant ID as a key. Also, if you want to write code that saves documents, you can include the tenant ID in the file name or location, for example. In those cases, you can use the TENANTID method in combination with the COMPANYNAME method to identify the company and the tenant database.  
  
## Syntax  
  
```  
  
ID := TENANTID  
```  
  
## Property Value/Return Value  
 Type: Text  
  
 The ID of the tenant that has started the current session.  
  
## See Also  
 [Multitenant Deployment Architecture](../../deployment/Multitenant-Deployment-Architecture.md)   
 [COMPANYNAME Method \(Database\)](devenv-COMPANYNAME-Method-Database.md)   
 [Database Methods](devenv-database-methods.md)