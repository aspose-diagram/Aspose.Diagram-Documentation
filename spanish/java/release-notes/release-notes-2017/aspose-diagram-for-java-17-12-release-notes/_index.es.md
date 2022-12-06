---
title: Aspose.Diagram for Java 17.12 Notas de la versión
type: docs
weight: 10
url: /es/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|Proporcione el único API para convertir una forma Visio a PDF|Mejora|
|DIAGRAMJAVA-50291|Proporcione el único API para convertir una forma Visio a HTML|Mejora|
|DIAGRAMJAVA-50572|El método Shape.connectedShapes no recupera los nodos salientes|Mejora|
|DIAGRAMJAVA-50391|Las imágenes y flechas volteadas se generan al convertir un VSD a SVG|Insecto|
|DIAGRAMJAVA-50570|VSD a PDF: se agregan los elementos de texto adicionales|Insecto|
|DIAGRAMJAVA-50571|Importar VSDX: se produjo un error en el elemento de forma|Insecto|
|DIAGRAMJAVA-50573|VSD a SVG: faltan las líneas de una forma de grupo|Insecto|
|DIAGRAMJAVA-50575|VSD a SVG: faltan elementos de texto|Insecto|
|DIAGRAMJAVA-50576|El procedimiento de importación VDX arroja un error de elemento de página|Insecto|
### **Agrega miembro de copia en la clase de forma**
El miembro de copia toma una instancia de forma de destino, como parámetro para clonar esta forma.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
### **Agrega un miembro toPdf en la clase Shape**
El miembro toPdf convierte una forma al formato PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Agrega al miembro HTML en la clase Shape**
El miembro toHTML convierte una forma al formato PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **Ejemplos de uso**
Consulte la lista de temas de ayuda agregados en los documentos Wiki Aspose.Diagram:

1. [Copie una forma Visio en otra instancia de forma](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [Convertir Visio Forma a PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [Convertir Visio Forma a HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


