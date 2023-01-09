---
title: Espacement automatique d'une collection de formes dans la page Visio
type: docs
weight: 30
url: /fr/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: Cette section explique comment espacer automatiquement une collection de formes dans une page visio avec Aspose.Diagram.
---
## **Espacement automatique d'une collection de formes dans la page Visio**
Avec Aspose.Diagram for .NET API, les développeurs peuvent espacer automatiquement une collection de formes dans le dessin Visio. Pour ce faire, la classe Page propose le membre AutoSpaceShapes qui prend les paramètres ShapeCollection et AutoSpaceOptions. La classe AutoSpaceOptions permet de définir des distances horizontales et verticales.
### **Espacer automatiquement les formes dans la page**
Utilisez le code suivant dans votre application .NET pour espacer automatiquement une collection de formes dans n'importe quelle page du dessin Visio.

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
