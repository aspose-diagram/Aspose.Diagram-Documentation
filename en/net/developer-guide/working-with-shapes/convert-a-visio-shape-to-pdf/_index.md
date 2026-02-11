---
title: Convert a Visio Shape To Pdf
type: docs
weight: 10
url: /net/convert-a-visio-shape-to-pdf/
description: This section explains how to convert a visio shape to pdf with Aspose.Diagram.
---

## **Convert a visio shape to pdf **
The ToPdf method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to convert to pdf.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to pdf.
### **Shape to Pdf**
Use the following code in your .net application to convert a visio shape to pdf.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Pdf
shape.ToPdf("out.pdf");

{{< /highlight >}}
```

