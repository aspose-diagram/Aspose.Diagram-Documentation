---
title: Público API Cambios en Aspose.Diagram 6.0.0
type: docs
weight: 50
url: /es/java/public-api-changes-in-aspose-diagram-6-0-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.9.0 a la 6.0.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **El método isGlued se agrega en la clase Shape**
El método isGlued toma un objeto de forma como parámetro para determinar si las dos formas están pegadas o no.
Código de ejemplo:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are glued

boolean glued = ShapedOne.isGlued(ShapedTwo);

{{< /highlight >}}
### **El método isConnected se agrega en la clase Shape**
El método isConnected toma un objeto de forma como parámetro para determinar si las dos formas están conectadas o no.
Código de ejemplo:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram

Diagram diagram = new Diagram("C:/temp/Drawing1.vsdx");

// get Visio page by name

Page page = diagram.getPages().getPage("Page-1");

// get Visio shapes by ids

Shape ShapedOne = page.getShapes().getShape(1);

Shape ShapedTwo = page.getShapes().getShape(2);

// determine whether shapes are connected

boolean connected = ShapedOne.isConnected(ShapedTwo);

{{< /highlight >}}
