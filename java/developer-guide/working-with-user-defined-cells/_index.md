---
title: Working with User-defined Cells
type: docs
weight: 100
url: /java/working-with-user-defined-cells/
---

## **Read User-defined Cells of the Visio Shapes**
Users insert text fields into shapes to display additional information. **User-defined Cells** is the one branch of these fields and this branch uses information entered in the Value cell of the User-defined Cells section in the shape's ShapeSheet. Developers can insert and read all user defined cells using [Aspose.Diagram for Java API](https://products.aspose.com/diagram/java).

The Users collection exposed by the [Shape](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Shape) class supports the com.aspose.diagram.User object. The [User](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/User) class can be used to read properties. There are a few user-defined cells as you can see in the following image:

**Table showing information about user defined cells** 

![todo:image_alt_text](working-with-user-defined-cells_1.png)

The following code is used to read user-defined cells.

The following image shows the output after running the code: 

![todo:image_alt_text](working-with-user-defined-cells_2.png)
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.java" >}}
### **Create User-defined Cell**
The Aspose.Diagram for Java API allows developers to create user-defined cell in the shapesheet. This example topic describes how to add as many user name rows as are needed, assign meaningful names to the rows, and set cell values.

The add method exposed by the Users collection can be used to create user-defined cell in the shapesheet. It takes a single parameter.

Use the following code in your Java application to create user-defined cell in the shapesheet using Aspose.Diagram for Java.
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
## **Retrieve User-defined Cells from Shapesheet**
Aspose.Diagram for Java API allows developers to retrieve user-defined cells from shapesheet. This example topic describes how to retrieve all user names for all shapes in a drawing.
### **Retrieve User-defined Cells**
The getNameU(), getValue().getVal() and getPrompt().getValue() methods exposed by the [User](https://apireference.aspose.com/diagram/java/com.aspose.diagram/User) class can be used to retrieve user-defined cells from shapesheet.
#### **Retrieve Cells from Shapesheet Programming Samples**
Use the following code in your Java application to retrieve all user-defined cells from shapesheet using Aspose.Diagram for Java.
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-UserDefinedCells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.java" >}}
