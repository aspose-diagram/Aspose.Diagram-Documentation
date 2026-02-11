---
title: Get Visio Shape Inherit Chars
type: docs
weight: 101
url: /net/get-visio-shape-inherit-chars/
description: This section explains how to get visio shape's font style inherited from it's parent style and master with Aspose.Diagram.
---
### **Retrieve Inherited Font Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit font data of a Visio shape. The InheritLine property, exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contains the line formatting values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Font Data Programming Sample**
The following code snippet retrieves the inherited font data of the shape. Please check this sample code:

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
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}
```

