---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a pocas líneas de código.
---
## **Exportación de diagramas a formatos de archivo de imagen**
Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando Aspose.Diagram para Python a través de Java.

Utilice el constructor de la clase Diagram para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible. La siguiente imagen muestra un archivo VSD a punto de guardarse en formato PNG. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

**[El archivo de ejemplo VSD.](ExportToImage.vsd)**

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.

**El archivo PNG de salida.**

![todo:imagen_alternativa_texto](ExportToImage.png)
### **Ejemplo de programación de exportación a archivo de imagen**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}