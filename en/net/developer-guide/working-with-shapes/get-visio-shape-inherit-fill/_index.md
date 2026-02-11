---
title: Get Visio Shape Inherit Fill
type: docs
weight: 100
url: /net/get-visio-shape-inherit-fill/
description: This section explains how to get visio shape's fill style inherited from it's parent style and master with Aspose.Diagram.
---
### **Retrieve Inherited Fill Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get the inherit Fill data of a Visio shape. The InheritFill property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contains the fill formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Fill Data Programming Sample**
The following code snippet retrieves the inherited fill data of the shape. Please check this sample code:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}
```

