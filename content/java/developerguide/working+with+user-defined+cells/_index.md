---
title : "Working with User-defined Cells" 
description : "" 
weight : 8043 
toc : false
type: docs
url: /java/developerguide/working+with+user-defined+cells/
---

# Aspose.Diagram for Java : Working with User-defined Cells


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Read User-defined Cells of the Visio Shapes](#read-user-defined-cells-of-the-visio-shapes)
{{< /panel >}}
    *   1.1.1 [Programming Samples](#WorkingwithUser-definedCells-ProgrammingSamples)
    
    *   1.2 [Create User-defined Cell](#WorkingwithUser-definedCells-CreateUser-definedCell)
        *   1.2.1 [Programming Samples](#WorkingwithUser-definedCells-ProgrammingSamples.1)
*   2 [Retrieve User-defined Cells from Shapesheet](#WorkingwithUser-definedCells-RetrieveUser-definedCellsfromShapesheet)
    *   2.1 [Retrieve User-defined Cells](#WorkingwithUser-definedCells-RetrieveUser-definedCells)
        *   2.1.1 [Retrieve Cells from Shapesheet Programming Samples](#WorkingwithUser-definedCells-RetrieveCellsfromShapesheetProgrammingSamples)
        *   2.1.2 [Programming Samples](#WorkingwithUser-definedCells-ProgrammingSamples.2)

 

 

## Read User-defined Cells of the Visio Shapes

Users insert text fields into shapes to display additional information. **User-defined Cells** is the one branch of these fields and this branch uses information entered in the Value cell of the User-defined Cells section in the shape's ShapeSheet. Developers can insert and read all user defined cells using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java).

The `Users` collection exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) class supports the `com.aspose.diagram.User` object. The [`User`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/User) class can be used to read properties. There are a few user-defined cells as you can see in the following image:

**Table showing information about user defined cells**  
![image](18809031.png)

The following code is used to read user-defined cells.

The following image shows the output after running the code:  
![image](18809030.png)

#### Programming Samples

### Create User-defined Cell

The Aspose.Diagram for Java API allows developers to create user-defined cell in the shapesheet. This example topic describes how to add as many user name rows as are needed, assign meaningful names to the rows, and set cell values.

The `add` method exposed by the `Users` collection can be used to create user-defined cell in the shapesheet. It takes a single parameter.

Use the following code in your Java application to create user-defined cell in the shapesheet using Aspose.Diagram for Java.

#### Programming Samples

## Retrieve User-defined Cells from Shapesheet

Aspose.Diagram for Java API allows developers to retrieve user-defined cells from shapesheet. This example topic describes how to retrieve all user names for all shapes in a drawing.

### Retrieve User-defined Cells

The `getNameU()`, `getValue().getVal()` and `getPrompt().getValue()` methods exposed by the [`User`](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/User) class can be used to retrieve user-defined cells from shapesheet.

#### Retrieve Cells from Shapesheet Programming Samples

Use the following code in your Java application to retrieve all user-defined cells from shapesheet using Aspose.Diagram for Java.

#### Programming Samples

