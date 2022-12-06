---
title: Público API Cambios en Aspose.Diagram 5.8.0
type: docs
weight: 20
url: /es/java/public-api-changes-in-aspose-diagram-5-8-0/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 5.7.0 a la 5.8.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **La opción SaveToolBar se agrega en HTMLSaveOptions**
Se ha agregado la nueva opción SaveToolBar en la clase HTMLSaveOptions. Especifica si guardar la barra de herramientas o no. El valor por defecto es verdadero. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // initialize HTMLSaveOptions class object

HTMLSaveOptions opts = new HTMLSaveOptions();

// set save toolbar option

opts.setSaveToolBar(false);

{{< /highlight >}}
### **VSDX Se agrega la opción de guardado en SaveFileFormat**
Anteriormente, Aspose.Diagram API admitía la lectura del formato VSDX, pero ahora hemos agregado soporte para escribir diagramas en el formato VSDX. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSDX format

diagram.save("C:\\temp\\Output.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Se ha agregado el método de grupo en la clase ShapeCollection**
Los desarrolladores ahora pueden agrupar varias formas juntas en Visio diagram usando Aspose.Diagram API. Códigos de ejemplo:

**Java**

{{< highlight "java" >}}

 // load a Visio diagram

Diagram diagram = new Diagram("c:\\temp\\test.vsd");

// Initialize an array of shapes

Shape[]shapes = new Shape[2];

// extract and assign shapes to the array

shapes[0]= diagram.getPages().get(0).getShapes().getShape(1);

shapes[1]= diagram.getPages().get(0).getShapes().getShape(2);

// mark array shapes as group

diagram.getPages().get(0).getShapes().group(shapes);

// save visio diagram

diagram.save("c:\\temp\\out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
