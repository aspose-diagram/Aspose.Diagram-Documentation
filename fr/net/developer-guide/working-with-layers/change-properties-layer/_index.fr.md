---
title: Modifier les propriétés du calque
type: docs
weight: 130
url: /fr/net/change-properties-layer/
description: Cette section explique comment modifier les propriétés du calque avec Aspose.Diagram.
---
## **Modifier les propriétés de la couche dans Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permet de modifier les propriétés du calque dans Microsoft Office Visio diagram.Chaque forme peut appartenir à plusieurs calques afin que les développeurs puissent modifier les propriétés du calque en fonction des besoins de l'utilisateur final. La[Feuille de page](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)L'objet de classe propose des calques qui permettent d'ajouter et de supprimer des objets de calque dans le dessin Visio. Les utilisateurs peuvent gérer[Couche](https://reference.aspose.com/diagram/net/aspose.diagram/layer) propriétés par programmation en utilisant Aspose.Diagram API comme suit :
### **Modifier l'exemple de programmation des propriétés de la couche**
Le morceau de code suivant aide à modifier les propriétés de la couche.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```