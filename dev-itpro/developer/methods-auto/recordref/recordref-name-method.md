---
title: "Name Method"
ms.author: solsen
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
author: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# Name Method
Identifies the name of the table

## Syntax
```
Name :=   RecordRef.Name()
```
> [!NOTE]  
> This method can be invoked using property access syntax.  

## Parameters
*RecordRef*  
&emsp;Type: [RecordRef](recordref-data-type.md)  
An instance of the [RecordRef](recordref-data-type.md) data type.  

## Return Value
*Name*  
&emsp;Type: [String](../string/string-data-type.md)  
The name of the table.  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
 This method works the same as the [TABLENAME Method \(Record\)](../../methods/devenv-tablename-method-record.md).  
  
## Example  
 The following example opens a table as a RecordRef variable that is named MyRecordRef. You can specify any table number in the [OPEN Method \(RecordRef\)](../../methods/devenv-open-method-recordref.md). In this example, the table 18 \(Customer\) is open. The NAME method retrieves the name of table 18 and stores it in the varTableName variable. The table number and name are displayed in a message box. This example requires that you create the following variables global text constant.  
  
|Variable name|DataType|  
|-------------------|--------------|  
|MyRecordRef|RecordRef|  
|varTableName|Text|  
  
|Text constant name|DataType|ENU value|  
|------------------------|--------------|---------------|  
|Text000|Text|Table %1 is the %2 table.|  
  
```  
  
TableNo := 18;  
MyRecordRef.OPEN(TableNo);  
varTableName := MyRecordRef.NAME;  
MESSAGE(Text000, TableNo, varTableName);  
```  

## See Also
[RecordRef Data Type](recordref-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)