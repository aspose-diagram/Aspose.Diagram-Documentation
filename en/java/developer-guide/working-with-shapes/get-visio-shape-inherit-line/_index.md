---
title: Get Visio Shape Inherit Line
type: docs
weight: 100
url: /java/get-visio-shape-inherit-line/
description: This section explains how to get visio shape's line style inherited from it's parent style and master with Aspose.Diagram.
---
### **Retrieve Inherited Line Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit line data of a Visio shape. The InheritLine property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contains the line formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Line Data Programming Sample**
The following code snippet retrieves the inherited line data of the shape. Please check this sample code:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedLine.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Line from the parent style and master
Line line = shape.getInheritLine();
// Get the line formatting values
System.out.println(line.getBeginArrow().getValue());
System.out.println(line.getBeginArrowSize().getValue());
System.out.println(line.getEndArrow().getValue());
System.out.println(line.getEndArrowSize().getValue());
System.out.println(line.getLineColor().getValue());
System.out.println(line.getLinePattern().getValue());
System.out.println(line.getLineWeight().getValue());
System.out.println(line.getRounding().getValue());

{{< /highlight >}}


