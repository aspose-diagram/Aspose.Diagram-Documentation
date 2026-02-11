---
title: Holen Sie sich Visio Shape Inherit Fill
type: docs
weight: 100
url: /de/net/get-visio-shape-inherit-fill/
description: In diesem Abschnitt wird erläutert, wie Sie den Füllstil der visio-Form erhalten, der vom übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Fülldaten einer Visio-Form ab**
Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler erhalten möglicherweise die vererbten Fülldaten einer Visio-Form. Die InheritFill-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse, enthält die Füllformatierungswerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Fülldaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Fülldaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

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

