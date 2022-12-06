---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/python-net/convert-visio-to-image/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a varios formatos de imágenes. Convierta Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM a imágenes PNG, JPEG, BMP con unas pocas líneas de código.
---
## **Exportar diagramas a formatos de archivo de imagen**
 Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/python-net/) API. Use el constructor de clase [Diagram] para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible.

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.
### **Exportar Microsoft Visio Dibujo a archivo de imagen**
{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToImage.py" >}}

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportPageToImage.py" >}}