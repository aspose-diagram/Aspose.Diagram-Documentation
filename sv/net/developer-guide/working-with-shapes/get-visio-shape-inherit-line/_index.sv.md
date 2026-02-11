---
title: Skaffa Visio Shape Inherit Line
type: docs
weight: 100
url: /sv/net/get-visio-shape-inherit-line/
description: Det här avsnittet förklarar hur du får visio-formens linjestil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvd linjedata från en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvningslinjedata för en Visio-form. Egenskapen InheritLine, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, innehåller linjeformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt linjedataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda linjedata. Kontrollera denna exempelkod:

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

