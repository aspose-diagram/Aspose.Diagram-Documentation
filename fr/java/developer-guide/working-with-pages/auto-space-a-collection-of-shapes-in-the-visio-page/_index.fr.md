---
title: Espacement automatique d'une collection de formes dans la page Visio
type: docs
weight: 30
url: /fr/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Espacement automatique d'une collection de formes dans la page Visio**
Avec Aspose.Diagram for Java API, les développeurs peuvent espacer automatiquement une collection de formes dans le dessin Visio. Pour ce faire, la classe Page propose le membre autoSpaceShapes qui prend les paramètres ShapeCollection et AutoSpaceOptions. La classe AutoSpaceOptions permet de définir des distances horizontales et verticales.
### **Espacer automatiquement les formes dans la page**
Utilisez le code suivant dans votre application Java pour espacer automatiquement une collection de formes dans n'importe quelle page du dessin Visio.

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
