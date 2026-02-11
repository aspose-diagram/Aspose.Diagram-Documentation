---
title: Skaffa Visio Shape Inherit Fill
type: docs
weight: 100
url: /sv/net/get-visio-shape-inherit-fill/
description: Det här avsnittet förklarar hur du får visio-formens fyllningsstil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvd fyllningsdata för en Visio-form**
Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan få ärvde Fill-data för en Visio-form. Egenskapen InheritFill, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, innehåller fyllningsformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:


{{< highlight csharp >}}
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


