---
title: Modifier la taille de la page
type: docs
weight: 10
url: /fr/java/change-page-size/
description: Cette section explique comment modifier la taille de la page dans un fichier visio avec Aspose.Diagram.
---
## **Modifier la taille de la page**

 La[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)L'objet représente la zone de dessin d'une page de premier plan ou d'une page d'arrière-plan. La propriété Pages exposée par le[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) prend en charge une collection d'objets Aspose.Diagram.Page.
 La[Accessoires de page](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) L'objet représente les attributs de la page, tels que la largeur, la hauteur et l'échelle de la page. Cette propriété peut être utilisée pour modifier la taille de la page.

Utilisez la propriété PageProps pour modifier la taille de la page .
### **Définir un exemple de programmation de taille de page**
Le morceau de code suivant change la taille de la page à partir d'un diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

