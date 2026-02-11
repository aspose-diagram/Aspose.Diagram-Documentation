---
title: Get Visio Shape Inherit Line
type: docs
weight: 100
url: /net/get-visio-shape-inherit-line/
description: This section explains how to get visio shape's line style inherited from it's parent style and master with Aspose.Diagram.
---
### **Retrieve Inherited Line Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit line data of a Visio shape. The InheritLine property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contains the line formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Line Data Programming Sample**
The following code snippet retrieves the inherited line data of the shape. Please check this sample code:

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
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}
```

