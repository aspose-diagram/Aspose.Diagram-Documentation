---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportación de diagramas a formatos de archivo de imagen**
This article explains how to export a Microsoft Visio diagram to an image using Aspose.Diagram for Python via Java.

Use the Diagram class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

**[El archivo de ejemplo VSD.](ExportToImage.vsd)**

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.

**El archivo de salida PNG.**

![todo:imagen_alternativa_texto](ExportToImage.png)
### **Ejemplo de programación de exportación a archivo de imagen**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}