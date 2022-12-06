---
title: Guarde el documento Visio mediante programación
linktitle: Guardar documento Visio
type: docs
weight: 30
url: /es/net/save-visio-document/
description: Esta página describe cómo guardar el documento Visio en un archivo, transmitir con la biblioteca Aspose.Diagram.
---
## **Visio Dibujo Guardar Resumen**
 Utilizar el[Diagram.Save]() método para guardar un dibujo Microsoft Visio. Hay sobrecargas que permiten guardar un dibujo en un archivo. El dibujo se puede guardar en cualquier formato de guardado admitido por Aspose.Diagram. Para ver la lista de todos los formatos de guardado admitidos, consulte el[Guardar formato de archivo]() enumeración
## **Ahorro Visio Diagram**
 La clase Diagram de Aspose.Diagram API representa un dibujo Visio y los desarrolladores pueden guardar su objeto Visio diagram en cualquier formato de archivo compatible. Para guardar un archivo Microsoft Visio, simplemente use el[Diagram.Save]()método, acepta un nombre de archivo con una ruta completa o un objeto de flujo de archivo. Aspose.Diagram API infiere el formato de guardado de la extensión del archivo y también ofrece un parámetro SaveFileFormat adicional para especificar el formato del archivo de salida.
### **Guarde un Visio Diagram en cualquier formato de archivo compatible**
Usando Aspose.Diagram API, los desarrolladores pueden guardar un Visio diagram en cualquier formato de archivo compatible como se indica a continuación:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF y XAML**
### **Guardando Diagram Ejemplo de programación**
El siguiente ejemplo guarda un documento en un archivo.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Especificación de las opciones de guardado de Visio**
 Hay varios[Diagram.Save]() sobrecargas de métodos que aceptan un objeto SaveOptions. Este debería ser un objeto de una clase derivada de la clase SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado. Por ejemplo, hay PdfSaveOptions para el formato de guardado SaveFileFormat.PDF.
### **Visio Diagram Opciones de guardado**
Estos ejemplos muestran cómo:

- [Usar Diagram Opciones de guardado](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Usar opciones de guardado de PDF](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Usar opciones de guardado de HTML](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Usar opciones para guardar imágenes](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Usar opciones de guardado de SVG](https://docs.aspose.com/diagram/net/save-visio-document/).
- [Utilice las opciones de guardado de SWF](https://docs.aspose.com/diagram/net/save-visio-document/).
#### **Uso de las opciones de guardado Diagram**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.cs" >}}



#### **Uso de las opciones de guardado de PDF**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.cs" >}}



#### **Uso de las opciones de guardado de HTML**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato de archivo HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.cs" >}}



#### **Uso de las opciones para guardar imágenes**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato de archivo de imagen.



{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.cs" >}}


Uso de las opciones de guardado de SVG

El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.cs" >}}


Uso de las opciones de guardado de SWF

El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato SWF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UseSWFSaveOptions-UseSWFSaveOptions.cs" >}}

A veces, los desarrolladores necesitan guardar o exportar diagramas Visio a diferentes formatos de archivo mediante programación (como VDX, PDF, JPEG, etc.).
## **Guarde el archivo VSD en diferentes formatos de archivo (VDX, PDF y JPEG)**
 Este artículo proporciona un ejemplo de código que ilustra cómo usar[VSTO](https://docs.aspose.com/diagram/net/save-visio-document/) y[Aspose.Diagram for .NET](https://docs.aspose.com/diagram/net) para guardar un archivo Microsoft Visio VSD en un archivo VDX, un archivo PDF o un archivo JPEG mediante programación. A continuación se muestran fragmentos de código paralelo para VSTO y Aspose.Diagram for .NET que explican cómo guardar un archivo VSD en diferentes formatos de archivo. Notarás que el código Aspose.Diagram es más corto. Siéntase libre de usar el código y cambiarlo para satisfacer sus necesidades específicas.
### **Guardar un archivo VSD en otros formatos con VSTO**
VSTO le permite programar con archivos Microsoft Visio. Para guardar un archivo en otros formatos:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Cargue el diagram.
1. Guardar en VDX, PDF y JPEG.
1. Salga del objeto de aplicación Visio.
#### **Guardar un archivo VSD con muestra de programación VSTO**
{{% alert color="primary" %}} 

usando Visio = Microsoft.Office.Interop.Visio;
Importaciones Visio = Microsoft.Office.Interop.Visio

{{% /alert %}} 

**Ejemplo:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withVSTO-SaveDiagramTo_VDX_PDF_JPEG_withVSTO.cs" >}}
### ` `**Guardar archivo VSD en otros formatos con Aspose.Diagram for .NET**
Usando Aspose.Diagram, los desarrolladores no necesitan Microsoft Office Visio en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Los fragmentos de código a continuación muestran cómo:

1. Cargue un diagram.
1. Guarde el diagram al VSX, PDF y JPEG.
#### **Guardando el archivo VSD con Aspose.Diagram for .NET Ejemplo de programación**
{{% alert color="primary" %}} 

usando Aspose.Diagram;
Importaciones Aspose.Diagram

{{% /alert %}} 

**Ejemplo:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-SaveDiagramTo-VDX-PDF-JPEG-withAspose-SaveDiagramTo_VDX_PDF_JPEG_withAspose.cs" >}}
