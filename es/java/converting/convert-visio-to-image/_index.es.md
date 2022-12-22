---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Exportación de diagramas a formatos de archivo de imagen**
 Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizar el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
**El archivo fuente. Tenga en cuenta que las etiquetas de flecha y triángulo están en negrita.**

![todo:imagen_alternativa_texto](http://i.imgur.com/WOV36ek.png)

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.

**El archivo de salida PNG.**

![todo:imagen_alternativa_texto](http://i.imgur.com/WOV36ek.png)
### **Ejemplo de programación de exportación a archivo de imagen**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}