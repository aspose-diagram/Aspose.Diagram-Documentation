---
title: Vérifier l'expansion automatique de la page
type: docs
weight: 10
url: /fr/net/check-page-autoexpand/
description: Cette section explique comment vérifier ou modifier l'expansion automatique de la page dans un fichier visio avec Aspose.Diagram.
---
## **Modifier la taille de la page**

 La[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) prend en charge une collection d'objets Aspose.Diagram.Page.
 La[Accessoires de page](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) L'objet représente les attributs de la page, tels que la largeur, la hauteur et l'échelle de la page. Cette propriété peut être utilisée pour vérifier l'expansion automatique de la page.

Utilisez la propriété PageProps pour vérifier l'expansion automatique de la page.
### **Définir un exemple de programmation de taille de page**
Le morceau de code suivant vérifie l'expansion automatique de la page à partir d'un diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

