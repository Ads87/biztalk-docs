---
description: "Learn more about: Content Type (Node Property of All Schemas)"
title: Content Type (Node Property of All Schemas)
TOCTitle: Content Type (Node Property of All Schemas)
ms:assetid: db67f54d-cb33-4a25-9893-8ddbca7f3fe2
ms:mtpsurl: https://msdn.microsoft.com/library/Aa561409(v=BTS.80)
ms:contentKeyID: 51531702
ms.date: 08/30/2017
mtps_version: v=BTS.80
---

# Content Type (Node Property of All Schemas)

 

Use the **Content Type** property to define whether the content of the **Record** node is simple or complex. Simple content is data only, and complex content is subelements.

## Applies to Nodes of Type

[Record](record-node-properties.md)

## Category

Advanced

## Allowed Values

<table>
<thead>
<tr class="header">
<th>Drop-down list choice</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>(Default)</strong></td>
<td>Use this value in conjunction with a blank value for the <a href="base-data-type-node-property-of-all-schemas.md">Base Data Type</a> property to indicate a default interpretation (defined by XSD) of complex content that restricts <strong>anyType</strong>.<br />
<br />
A blank value for <strong>Base Data Type</strong> property forces this property to the <strong>(Default)</strong> value and setting this property to <strong>(Default)</strong> forces the <strong>Base Data Type</strong> property to a blank value.</td>
</tr>
<tr class="even">
<td><strong>ComplexContent</strong></td>
<td>Specifies that content in the selected <strong>Record</strong> node can include subelements.</td>
</tr>
<tr class="odd">
<td><strong>SimpleContent</strong></td>
<td>Specifies that content in the selected <strong>Record</strong> node is derived from a simple type. This means that it can contain only attributes and text that conform to the derived data type. In other words, it cannot contain subelements.</td>
</tr>
</tbody>
</table>


## Default Value

**(Default)**, indicating that there is no specified content type for the element that corresponds to this **Record** node, indicating a default interpretation (defined by XSD) of complex content that restricts **anyType**.

## XSD Persistence

When set to other than the default value, represented within the **complexType** element of the **Record** node using a nested pair of elements: an **extension** or **restriction** element within a **simpleContent** or **complexContent** element. The **base** attribute of the **extension** or **restriction** element is set to the value of the [Base Data Type](base-data-type-node-property-of-all-schemas.md) property.

For more information about these persistence permutations, see the XSD Persistence section of [Derived By (Node Property of All Schemas)](derived-by-node-property-of-all-schemas.md).

## Remarks

You can examine and set this property in the Visual Studio Properties window when you select a **Record** node (including a root **Record** node) in BizTalk Editor.

The setting of this property interacts with the [Base Data Type](base-data-type-node-property-of-all-schemas.md) and [Derived By](derived-by-node-property-of-all-schemas.md) properties.

Simple content includes only attributes and text data. Complex content includes elements, attributes, and if the [Mixed](mixed-node-property-of-all-schemas.md) property is set to **True**, text data.

## See Also

[Node Properties of All Schemas](node-properties-of-all-schemas.md)

