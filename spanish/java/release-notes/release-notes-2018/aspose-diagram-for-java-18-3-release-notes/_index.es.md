---
title: Aspose.Diagram for Java 18.3 Notas de la versión
type: docs
weight: 100
url: /es/java/aspose-diagram-for-java-18-3-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for Java 18.3](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-3-release-notes/).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50592|Agregar soporte de las instrucciones de procesamiento NewValue|Mejora|
|DIAGRAMJAVA-50150|No se puede acceder a los objetos TabsCollection de forma|Insecto|
|DIAGRAMJAVA-50588|Salida VSDX: se agrega una forma de gran tamaño|Insecto|
|DIAGRAMJAVA-50593|VSDX a SVG: texto y colores de fondo incorrectos|Insecto|
|DIAGRAMJAVA-50595|Diagram cambia a blanco y negro al guardar el documento VSDX|Insecto|
### **Agrega el miembro moveTo en la clase de página**
El miembro moveTo toma el índice de la página de destino como parámetro para mover la posición de la página en el dibujo Visio.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

1. [Mover posición de página en el dibujo Visio]
