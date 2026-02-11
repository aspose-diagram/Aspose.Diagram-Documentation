---
title: Holen Sie sich Visio Shape Inherit Line
type: docs
weight: 100
url: /de/net/get-visio-shape-inherit-line/
description: In diesem Abschnitt wird erläutert, wie Sie den Linienstil der visio-Form erhalten, der von seinem übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Liniendaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die Erbliniendaten einer Visio-Form abrufen oder festlegen. Die InheritLine-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, enthält die Linienformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Leitungsdaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Liniendaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

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

