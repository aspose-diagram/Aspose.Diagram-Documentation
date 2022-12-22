---
title: Guarde el documento Visio mediante programación
linktitle: Guardar documento Visio
type: docs
weight: 30
url: /es/python-net/save-visio-document/
description: Esta página describe cómo guardar el documento Visio en un archivo, transmitir con la biblioteca Aspose.Diagram.
---
## **Visio Dibujo Guardar Resumen**
 Utilizar el[Diagram.Save]() método para guardar un dibujo Microsoft Visio. Hay sobrecargas que permiten guardar un dibujo en un archivo. El dibujo se puede guardar en cualquier formato de guardado admitido por Aspose.Diagram. Para ver la lista de todos los formatos de guardado admitidos, consulte el[Guardar formato de archivo]() enumeración
## **Ahorro Visio Diagram**
 La clase Diagram de Aspose.Diagram API representa un dibujo Visio y los desarrolladores pueden guardar su objeto Visio diagram en cualquier formato de archivo compatible. Para guardar un archivo Microsoft Visio, simplemente use el[Diagram.Save]()método, acepta un nombre de archivo con una ruta completa o un objeto de flujo de archivo. Aspose.Diagram API infiere el formato de guardado de la extensión del archivo y también ofrece un parámetro SaveFileFormat adicional para especificar el formato del archivo de salida.
### **Guarde un Visio Diagram en cualquier formato de archivo compatible**
Usando Aspose.Diagram API, los desarrolladores pueden guardar un Visio diagram en cualquier formato de archivo compatible como se indica a continuación:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Guardando Diagram Ejemplo de programación**
El siguiente ejemplo guarda un documento en un archivo.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Especificación de las opciones de guardado de Visio**
 Hay varios[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Opciones de guardado**
Estos ejemplos muestran cómo:

- [Usar Diagram Opciones de guardado](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usar PDF Opciones de guardado](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usar HTML Opciones de guardado](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usar opciones para guardar imágenes](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usar SVG Opciones de guardado](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usar SWF Opciones de guardado](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Uso de las opciones de guardado Diagram**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato Visio.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseDiagramSaveOptions.py" >}}



#### **Uso de las opciones de guardado PDF**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UsePdfSaveOptions.py" >}}



#### **Uso de las opciones de guardado HTML**
The code below shows how to set save options before saving a document to HTML file format.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseHtmlSaveOptions.py" >}}



#### **Uso de las opciones para guardar imágenes**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato de archivo de imagen.



{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseImageSaveOptions.py" >}}


Uso de las opciones de guardado SVG

El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato SVG.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseSvgSaveOptions.py" >}}

Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

### ` `**Saving VSD File to Other Formats with Aspose.Diagram for Python via .NET**
Usando Aspose.Diagram, los desarrolladores no necesitan Microsoft Office Visio en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Los fragmentos de código a continuación muestran cómo:

1. Cargue un diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for Python via .NET Programming Sample**
{{% alert color="primary" %}} 

importar aspose.diagram
de aspose.diagram importar *

{{% /alert %}} 

**Ejemplo:**

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-SaveDiagramTo_VDX_PDF_JPEG_withAspose.py" >}}
