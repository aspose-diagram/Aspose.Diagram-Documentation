---
title: Aspose.Diagram for Java 17.10 Notas de la versión
type: docs
weight: 30
url: /es/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 Esta página contiene notas de la versión para[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|JpegQuality no tiene ningún efecto en el documento de salida|Mejora|
|DIAGRAMJAVA-50548|Salida VSDX: la línea de conexión que pasa por el límite de la forma|Insecto|
|DIAGRAMJAVA-50550|La sección Shape Transform no conserva las fórmulas|Insecto|
|DIAGRAMJAVA-50551|VSDX a PNG: representación incorrecta de las esquinas de la forma|Insecto|
|DIAGRAMJAVA-50552|Los colores de relleno no se conservan al guardar un dibujo Visio en SVG|Insecto|
|DIAGRAMJAVA-50553|Representación incorrecta de líneas al guardar un dibujo Visio en SVG|Insecto|
|DIAGRAMJAVA-50554|Los colores de relleno no se conservan al guardar un dibujo Visio en SVG|Insecto|
|DIAGRAMJAVA-50555|Representación incorrecta de líneas al guardar un dibujo Visio en SVG|Insecto|
|DIAGRAMJAVA-50559|VSDM a VDX - las líneas de conexión no están conectadas a las formas|Insecto|
|DIAGRAMJAVA-50561|El dibujo VSDX está dañado después de agregar el elemento SolutionXML|Insecto|
### **Agrega SameAsPdfConversionArea en ImageSaveOptions**
Especifica si guardar el área de la misma manera que PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
