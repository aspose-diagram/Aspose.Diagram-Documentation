---
title: Vérifier l'expansion automatique de la page
type: docs
weight: 10
url: /fr/java/check-page-autoexpand/
description: Cette section explique comment vérifier ou modifier l'expansion automatique de la page dans un fichier visio avec Aspose.Diagram.
---
## **Vérifier l'expansion automatique de la page**

 La[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) prend en charge une collection d'objets Aspose.Diagram.Page.
 La[Accessoires de page](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) L'objet représente les attributs de la page, tels que la largeur, la hauteur et l'échelle de la page. Cette propriété peut être utilisée pour vérifier l'expansion automatique de la page.

Utilisez la propriété PageProps pour vérifier l'expansion automatique de la page.
### **Exemple de programmation d'expansion automatique de page de vérification**
Le morceau de code suivant vérifie l'expansion automatique de la page à partir d'un diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
