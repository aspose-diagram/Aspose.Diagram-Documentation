---
title:  Convertir Visio a formatos de imágenes
linktitle: Convertir Visio a Imágenes
type: docs
weight: 20
url: /es/java/convert-visio-to-image/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a varios formatos de imágenes. Convierta Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM a imágenes PNG, JPEG, BMP con unas pocas líneas de código.
---
## **Exportación de diagramas a formatos de archivo de imagen**
 Este artículo explica cómo exportar un Microsoft Visio diagram a una imagen usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizar el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' para leer los archivos diagram y el método Save para exportar el diagram a cualquier formato de imagen compatible. La siguiente imagen muestra un archivo VSD a punto de guardarse en formato PNG. También puede usar otros formatos diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).
**El archivo fuente. Tenga en cuenta que las etiquetas de flecha y triángulo están en negrita.**

![todo:imagen_alternativa_texto](http://i.imgur.com/WOV36ek.png)

Para exportar un diagram a una imagen:

- Cree una instancia de la clase Diagram.
- Llame al método Guardar de la clase Diagram y configure el formato de imagen al que desea exportar. El archivo de imagen de salida se parece al archivo original.

**El archivo PNG de salida.**

![todo:imagen_alternativa_texto](http://i.imgur.com/WOV36ek.png)
### **Ejemplo de programación de exportación a archivo de imagen**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

También es posible guardar una página en particular en la imagen, en lugar de todo el documento:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}