---
title:  Convertir Visio a formato PDF
linktitle: Convertir Visio a PDF
type: docs
weight: 10
url: /es/python-net/convert-visio-to-pdf/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a formatos PDF. Convierta VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM a PDF con unas pocas líneas de código.
---
## **Exportar a PDF**
{{% alert color="primary" %}}

Aspose.Diagram para Python a través de .NET escribe directamente la información sobre API y el número de versión en los documentos de salida. Por ejemplo, al renderizar un Dibujo a PDF, Aspose.Diagram for .NET se completa**Solicitud** campo con valor 'Aspose.Diagram' y**Productor de PDF** campo con valor, por ejemplo, 'Aspose.Diagram 17.9'.

Tenga en cuenta que no puede indicar al Aspose.Diagram for .NET API que cambie o elimine esta información de los documentos de salida.

{{% /alert %}}

 Este artículo explica cómo exportar un Microsoft Visio diagram a PDF usando[Aspose.Diagram para Python vía .NET](https://products.aspose.com/diagram/python-net/) API.

Use el constructor de clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

La siguiente imagen muestra el VSD diagram que los fragmentos de código debajo exportan PDF. También puede usar otros formatos diagram (VSS, VSSM, VDX, VST, VSTX, VDX, VTX o VSX).

|**El archivo fuente.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_1.png)|


Para exportar VSD diagram a PDF:

1. Cree una instancia de la clase Diagram.
1. Llame al método Guardar de clases Diagram y establezca el formato de salida en PDF.

A continuación se muestra una imagen del archivo PDF de salida.

|**El archivo PDF de salida.**|
|:- |
|![todo:imagen_alternativa_texto](how-to-convert-a-visio-diagram_2.png)|
### **Exportar Microsoft Visio Dibujo a PDF**
Los ejemplos de código muestran cómo exportar el dibujo Microsoft Visio a PDF usando Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
