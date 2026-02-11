---
title: Convert a Visio Shape To Html
type: docs
weight: 10
url: /java/convert-a-visio-shape-to-html/
description: This section explains how to convert a visio shape to html with Aspose.Diagram.
---

## **Convert a visio shape to html **
The ToHTML method exposed by the [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class can be used to convert to html.

The code below shows how to:

1. Load a sample diagram.
1. get a particular page.
1. get a particular shape.
1. convert shape to html.
### **Shape to Html**
Use the following code in your java application to convert a visio shape to html.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToHtml.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to HTML
HTMLSaveOptions hs = new HTMLSaveOptions();
shape.toHTML("out.htm", hs);
{{< /highlight >}}



