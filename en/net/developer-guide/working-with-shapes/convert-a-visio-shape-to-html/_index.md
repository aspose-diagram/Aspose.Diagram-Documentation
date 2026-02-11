---
title: Convert a Visio Shape To Html
type: docs
weight: 10
url: /net/convert-a-visio-shape-to-html/
description: This section explains how to convert a visio shape to html with Aspose.Diagram.
---

## **Convert a visio shape to html **
The ToHTML method exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class can be used to convert to html.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to html.
### **Shape to Html**
Use the following code in your .net application to convert a visio shape to html.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}


