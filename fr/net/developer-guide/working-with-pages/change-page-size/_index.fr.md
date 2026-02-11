---
title: Modifier la taille de la page
type: docs
weight: 10
url: /fr/net/change-page-size/
description: Cette section explique comment modifier la taille de la page dans un fichier visio avec Aspose.Diagram.
---
## **Modifier la taille de la page**

 La[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) prend en charge une collection d'objets Aspose.Diagram.Page.
 La[Accessoires de page](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) L'objet représente les attributs de la page, tels que la largeur, la hauteur et l'échelle de la page. Cette propriété peut être utilisée pour modifier la taille de la page.

Utilisez la propriété PageProps pour modifier la taille de la page .
### **Définir un exemple de programmation de taille de page**
Le morceau de code suivant change la taille de la page à partir d'un diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
