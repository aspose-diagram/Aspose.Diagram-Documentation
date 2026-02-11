---
title: Convert a Visio Shape To Image
type: docs
weight: 10
url: /java/convert-a-visio-shape-to-image/
description: This section explains how to convert a visio shape to image with Aspose.Diagram.
---

## **Convert a visio shape to image **
The ToImage method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class can be used to convert to image.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to image.
### **Shape to Image**
Use the following code in your java application to convert a visio shape to image.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}



