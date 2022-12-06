---
title: Espaciar automáticamente una colección de formas en la página Visio
type: docs
weight: 30
url: /es/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: Esta sección explica cómo autoespaciar una colección de formas en una página visio con Aspose.Diagram.
---
## **Espaciar automáticamente una colección de formas en la página Visio**
Con Aspose.Diagram for .NET API, los desarrolladores pueden espaciar automáticamente una colección de formas en el dibujo Visio. Para lograr esto, la clase Page ofrece el miembro AutoSpaceShapes que toma los parámetros ShapeCollection y AutoSpaceOptions. La clase AutoSpaceOptions permite establecer distancias horizontales y verticales.
### **Formas de espacio automático en la página**
Use el siguiente código en su aplicación .NET para autoespaciar una colección de formas en cualquier página del dibujo Visio.

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
