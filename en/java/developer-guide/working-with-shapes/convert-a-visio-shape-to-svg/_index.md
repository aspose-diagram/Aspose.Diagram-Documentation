---
title: Convert a Visio Shape To Svg
type: docs
weight: 10
url: /java/convert-a-visio-shape-to-svg/
description: This section explains how to convert a visio shape to svg with Aspose.Diagram.
---

## **Convert a visio shape to svg **
The ToSvg method exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class can be used to convert to svg.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to svg.
### **Shape to Svg**
Use the following code in your java application to convert a visio shape to svg.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}
```


