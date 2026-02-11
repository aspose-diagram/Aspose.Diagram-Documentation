---
title: Obtenir Visio Shape Inherit Fill
type: docs
weight: 100
url: /fr/net/get-visio-shape-inherit-fill/
description: Cette section explique comment obtenir le style de remplissage de la forme visio hérité de son style parent et maître avec Aspose.Diagram.
---
### **Récupérer les données de remplissage héritées d'une forme Visio**
Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir les données de remplissage héritées d'une forme Visio. La propriété InheritFill, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, contient les valeurs de formatage de remplissage pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de remplissage héritées**
L'extrait de code suivant récupère les données de remplissage héritées de la forme. Veuillez vérifier cet exemple de code :

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

