---
title: Obtenir Visio Shape Inherit Chars
type: docs
weight: 101
url: /fr/net/get-visio-shape-inherit-chars/
description: Cette section explique comment obtenir le style de police de la forme visio hérité de son style parent et maître avec Aspose.Diagram.
---
### **Récupérer les données de police héritées d'une forme Visio**
 Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de police héritées d'une forme Visio. La propriété InheritLine, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, contient les valeurs de formatage de ligne pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de police héritées**
L'extrait de code suivant récupère les données de police héritées de la forme. Veuillez vérifier cet exemple de code :

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

