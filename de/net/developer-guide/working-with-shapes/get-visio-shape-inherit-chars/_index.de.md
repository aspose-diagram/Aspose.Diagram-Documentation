---
title: Holen Sie sich Visio Form erben Zeichen
type: docs
weight: 101
url: /de/net/get-visio-shape-inherit-chars/
description: In diesem Abschnitt wird erläutert, wie Sie den Schriftstil der visio-Form erhalten, der von seinem übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Schriftdaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die Schriftartdaten einer Visio-Form abrufen oder festlegen. Die InheritLine-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, enthält die Linienformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Schriftdaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Schriftartdaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:


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


