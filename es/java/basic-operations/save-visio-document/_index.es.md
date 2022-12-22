---
title: Guarde el documento Visio mediante programación
linktitle: Guardar documento Visio
type: docs
weight: 30
url: /es/java/save-visio-document/
description: Esta página describe cómo guardar el documento Visio en un archivo, transmitir con la biblioteca Aspose.Diagram.
---
## **Visio Dibujo Guardar Resumen**
 Utilizar el[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) método para guardar un dibujo Microsoft Visio. Hay sobrecargas que permiten guardar un dibujo en un archivo. El dibujo se puede guardar en cualquier formato de guardado admitido por Aspose.Diagram. Para ver la lista de todos los formatos de guardado admitidos, consulte el[Guardar formato de archivo](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat) enumeración
## **Ahorro Visio Diagram**
 La clase Diagram de Aspose.Diagram API representa un dibujo Visio y los desarrolladores pueden guardar su objeto Visio diagram en cualquier formato de archivo compatible. Para guardar un archivo Microsoft Visio, simplemente use el[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)), acepta un nombre de archivo con la ruta completa o un objeto de flujo de archivo. Aspose.Diagram API infiere el formato de guardado de la extensión del archivo y también ofrece un parámetro SaveFileFormat adicional para especificar el formato del archivo de salida.
### **Guarde un Visio Diagram en cualquier formato de archivo compatible**
Usando Aspose.Diagram API, los desarrolladores pueden guardar un Visio diagram en cualquier formato de archivo compatible como se indica a continuación:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Guardando Diagram Ejemplo de programación**
El siguiente ejemplo guarda un documento en un archivo.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Especificación de las opciones de guardado de Visio**
 Hay varios[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Opciones de guardado**
Estos ejemplos muestran cómo:

- [Usar Diagram Opciones de guardado](/diagram/es/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Usar PDF Opciones de guardado](/diagram/es/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Usar HTML Opciones de guardado](/diagram/es/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Usar opciones para guardar imágenes](/diagram/es/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Usar SVG Opciones de guardado](/diagram/es/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Uso de las opciones de guardado Diagram**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Uso de las opciones de guardado PDF**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Uso de las opciones de guardado HTML**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Uso de las opciones para guardar imágenes**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en un formato de imagen.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Uso de las opciones de guardado SVG**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
