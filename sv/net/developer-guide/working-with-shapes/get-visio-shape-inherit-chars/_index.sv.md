---
title: Skaffa Visio Shape Inherit Chars
type: docs
weight: 101
url: /sv/net/get-visio-shape-inherit-chars/
description: Det här avsnittet förklarar hur du får visio-formens teckensnittsstil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvda teckensnittsdata för en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvte teckensnittsdata för en Visio-form. Egenskapen InheritLine, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, innehåller linjeformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt teckensnittsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda teckensnittsdata. Kontrollera denna exempelkod:

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

