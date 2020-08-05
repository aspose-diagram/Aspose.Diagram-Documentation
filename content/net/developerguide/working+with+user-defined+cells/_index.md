---
title : "Working with User-defined Cells" 
description : "" 
weight : 8047 
toc : false
type: docs
url: /net/developerguide/working+with+user-defined+cells/
---

# Aspose.Diagram for .NET : Working with User-defined Cells


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Read User-defined Cells of the Visio Shapes](#read-user-defined-cells-of-the-visio-shapes)
    *   1.1 [Retrieve the User-defined Cells Fields](#retrieve-the-user-defined-cells-fields)
        *   1.1.1 [Retrieve Cells Programming Sample](#retrieve-cells-programming-sample)
*   2 [Create User-defined Cell in the ShapeSheet](#create-user-defined-cell-in-the-shapesheet)
    *   2.1 [Create User-defined Cell](#create-user-defined-cell)
        *   2.1.1 [Create Cell Programming Sample](#create-cell-programming-sample)
*   3 [Retrieve User-defined Cells from Shapesheet](#retrieve-user-defined-cells-from-shapesheet)
    *   3.1 [Retrieve User-defined Cells](#retrieve-user-defined-cells)
        *   3.1.1 [Retrieve Cells from Shapesheet Programming Samples](#retrieve-cells-from-shapesheet-programming-samples)
{{< /panel >}}
 

 

## Read User-defined Cells of the Visio Shapes

Users insert text fields into shapes to display additional information. **User-defined Cells** is the one branch of these fields and this branch uses information entered in the Value cell of the User-defined Cells section in the shape's ShapeSheet. Developers can insert and read all user defined cells using [Aspose.Diagram for .NET API](http://www.aspose.com/.net/diagram-component.aspx).

### Retrieve the User-defined Cells Fields

Users collection exposed by [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class supports the `Aspose.Diagram.User` object. This property can be used to read the user defined cells of a Visio shape as available in the User-defined Cells section of the shape's ShapeSheet.  
![image](https://docs2.aspose.com/diagram/net/attachments/18350135/18546987.png)

#### Retrieve Cells Programming Sample

The following piece of code allows developers to read the user defined cells fields.

  
This image shows the output after running the above code:  
  
![image](https://docs2.aspose.com/diagram/net/attachments/18350135/18546990.png)

## Create User-defined Cell in the ShapeSheet

[Aspose.Diagram for .NET API](http://www.aspose.com/.net/diagram-component.aspx) allows to create user-defined cell in the shapesheet. This example topic describes the way, developers can add as many User.name rows as they need, assign meaningful names to the rows, and set cell values.

### Create User-defined Cell

The `Add` method exposed by the `Users` Collection can be used to create a user-defined cell in the shapesheet. It takes a single parameter.

#### Create Cell Programming Sample

Use the following code example in your .NET application to create user-defined cell in the shapesheet using Aspose.Diagram for .NET.

## Retrieve User-defined Cells from Shapesheet

Aspose.Diagram for .NET API allows to retrieve user-defined cells from shapesheet. This example topic describes the way, developers can retrieve all User.name for all shapes in a drawing.

### Retrieve User-defined Cells

The `NameU`, `Value.Val` and `Prompt.Value` properties exposed by the `User` class can be used to retrieve user-defined cells from shapesheet.

#### Retrieve Cells from Shapesheet Programming Samples

Use the following code in your .NET application to retrieve all user-defined cells from shapesheet using Aspose.Diagram for .NET.

