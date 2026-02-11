---
title: Obtenir la ligne d'héritage de forme Visio
type: docs
weight: 100
url: /fr/net/get-visio-shape-inherit-line/
description: Cette section explique comment obtenir le style de ligne de la forme visio hérité de son style parent et le maîtriser avec Aspose.Diagram.
---
### **Récupérer les données de ligne héritées d'une forme Visio**
 Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de ligne héritées d'une forme Visio. La propriété InheritLine, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, contient les valeurs de formatage de ligne pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de ligne héritées**
L'extrait de code suivant récupère les données de ligne héritées de la forme. Veuillez vérifier cet exemple de code :


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


