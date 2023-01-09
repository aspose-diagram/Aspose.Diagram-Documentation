---
title: Espaciar automáticamente una colección de formas en la página Visio
type: docs
weight: 30
url: /es/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Espaciar automáticamente una colección de formas en la página Visio**
Con Aspose.Diagram for Java API, los desarrolladores pueden espaciar automáticamente una colección de formas en el dibujo Visio. Para lograr esto, la clase Page ofrece el miembro autoSpaceShapes que toma los parámetros ShapeCollection y AutoSpaceOptions. La clase AutoSpaceOptions permite establecer distancias horizontales y verticales.
### **Formas de espacio automático en la página**
Use el siguiente código en su aplicación Java para autoespaciar una colección de formas en cualquier página del dibujo Visio.

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
