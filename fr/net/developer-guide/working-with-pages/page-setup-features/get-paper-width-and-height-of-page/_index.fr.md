---
title: Obtenir la largeur du papier et la hauteur de la page
type: docs
weight: 50
url: /fr/net/get-paper-width-and-height-of-page/
description: Cette section explique comment obtenir le format de papier de la page visio avec Aspose.Diagram.
---
## **Scénarios d'utilisation possibles**

Parfois, vous devez connaître la largeur et la hauteur du format de papier tel qu'il a été défini dans la mise en page de la page. Veuillez utiliser le[**PageProps.PageWidthPageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)et[**PageProps.PageHeightPageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)propriétés à cet effet.

## **Obtenir la largeur et la hauteur de la page Prop de la page**

 L'exemple de code suivant explique l'utilisation de[**PageProps.PageWidthPageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)et[**PageProps.PageHeightPageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)Propriétés.

### **Exemple de code**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}
```
