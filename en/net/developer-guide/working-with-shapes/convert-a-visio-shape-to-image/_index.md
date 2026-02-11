---
title: Convert a Visio Shape To Image
type: docs
weight: 10
url: /net/convert-a-visio-shape-to-image/
description: This section explains how to convert a visio shape to image with Aspose.Diagram.
---

## **Convert a visio shape to image**
This topic elaborates how developers can convert a visio shape to image using Aspose.Diagram.
The ToImage method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to convert to image.


The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to image.
#### **Shape to image Programming Sample**
Use the following code in your .net application to convert a visio shape to image.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}
```
