---
title:  Convertir Visio a formato HTML
linktitle: Convertir Visio a HTML
type: docs
weight: 30
url: /es/java/convert-visio-to-html/
description: Este tema le muestra cómo Aspose.Diagram permite convertir Visio a formatos html. Convierta VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM a html con unas pocas líneas de código.
---
## **Exportar Visio a HTML** **Exportar Visio a HTML**
 Este artículo explica cómo exportar un Microsoft Visio diagram a HTML usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizar el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) constructor de clase para leer los archivos diagram y el método Guardar para exportar el diagram a cualquier formato de imagen compatible. Los desarrolladores pueden guardar el HTML resultante en el almacenamiento local o directamente en una instancia de transmisión.

1. [Guarde el HTML resultante en el almacenamiento local](/diagram/es/java/how-to-convert-a-visio-diagram/).
1. [Guarde el HTML resultante en una instancia de flujo](/diagram/es/java/how-to-convert-a-visio-diagram/).

La siguiente imagen muestra un archivo VSD a punto de guardarse en formato PNG. También puede usar otros formatos diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX o 34711).

**Entrada diagram.**

![todo:imagen_alternativa_texto](http://i.imgur.com/YX4BNNq.png)

Para exportar VSD diagram a HTML, realice los siguientes pasos:

1. Cree una instancia de la clase Diagram.
1. Llame al método Save de la clase Dagram y establezca HTML como formato de salida.

La siguiente imagen muestra el archivo HTML de salida.

**Salida HTML diagram.**

![todo:imagen_alternativa_texto](http://i.imgur.com/syavUqI.png)
### **Guarde el HTML resultante en el almacenamiento local**
El archivo resultante se puede guardar pasando una cadena de ruta completa, incluido el nombre del archivo y la extensión, por ejemplo, @"c:\temp\MyOutput.html".
#### **Guardar HTML resultante en el ejemplo de programación de almacenamiento local**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Guarde el HTML resultante en una instancia de flujo**
Es un caso de uso para guardar el HTML resultante en una base de datos o repositorio sin almacenarlo en el almacenamiento local. Esta función también incorpora otros recursos resultantes del HTML, por ejemplo, fuentes, CSS (que contiene la información de estilo) e imágenes. Ya que guarda un solo archivo HTML en la instancia de flujo.
#### **Guardar HTML resultante en un ejemplo de programación de secuencias**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
