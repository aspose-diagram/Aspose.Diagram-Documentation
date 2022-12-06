﻿---
title: Introducción
type: docs
weight: 10
url: /es/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio guarda información sobre las acciones realizadas en un diagram dentro del archivo. Por ejemplo, la hora y la fecha en que se creó el documento, la última vez que se editó, imprimió o guardó, se guardan con el archivo. También se guarda información sobre qué versión de Microsoft Visio creó y editó por última vez el archivo.

Este artículo explica cómo recuperar esa información.

{{% /alert %}} 
## **Obtenga la versión de la biblioteca Aspose.Diagram for Java**
 El método getVersion() expuesto por el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class y el método getBuildNumberCreated() expuestos por el[Propiedades del documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class se utilizan para determinar la versión y el número de compilación completo de la instancia Microsoft Visio utilizada para crear el documento.
### **Determinar la versión de Microsoft Visio que creó, editó y guardó un documento**
 El método getBuildNumberEdited() expuesto por el[Propiedades del documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class se utiliza para determinar el número de compilación completo de la instancia Microsoft Visio utilizada para editar el documento.

Los métodos getTimeCreated(), getTimeEdited(), getTimePrinted() y getTimeSaved() expuestos por el[Propiedades del documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) class se utilizan para determinar la hora en que se creó, se editó por última vez, se imprimió por última vez y se guardó por última vez el documento Microsoft Visio.

También puede configurar estas propiedades para cambiar la información en el archivo.

Los ejemplos de código a continuación muestran cómo recuperar información sobre qué creó el archivo, así como cuándo se creó, editó, imprimió y guardó.

**La salida del código en una ventana de consola** 

![todo:imagen_alternativa_texto](introduction_1.png)
#### **Ejemplo de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **Escritura Microsoft Visio Resumen del documento Información**
Microsoft Visio le permite definir una serie de propiedades de información de resumen del documento para ayudarlo a usted y a sus colegas a identificar un diagram. Las propiedades de resumen, por ejemplo, título, tema, autor y descripción, hacen que el archivo sea más fácil de encontrar al buscar y más fácil de reconocer al navegar archivos

 los[Propiedades del documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)La clase expone una serie de propiedades para establecer u obtener información de resumen de Microsoft Visio diagram. Aspose.Diagram for Java puede actualizar la información de resumen del dibujo y luego volver a escribir el archivo de dibujo en VDX.

{{% alert color="primary" %}} 

Tenga en cuenta que no puede establecer valores contra el**Solicitud**y**Productor**porque Aspose Ltd. y Aspose.Diagram for Java xxx se mostrarán en estos campos.

{{% /alert %}} 
### **Escritura Microsoft Visio Resumen del documento Información**
Para actualizar la información de resumen del dibujo de un archivo VDX o VSD existente:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) clase.
1. Establezca las propiedades expuestas por el método Diagram.getDocumentProps() para definir la información de resumen para el archivo de dibujo Visio.
1. Llame al método save() de la clase Diagram para escribir el archivo de dibujo Visio en VDX.

Consulta la información resumida:

1. Abra el archivo de salida VDX en Microsoft Visio.
1.  Seleccionando**Información** desde el**Expediente** menú.

**El cuadro de diálogo Información que muestra la información de resumen actualizada** 

![todo:imagen_alternativa_texto](introduction_2.png)
#### **Ejemplo de programación**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **Detectar el formato de un archivo Visio**
 Usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, los desarrolladores pueden detectar el formato del archivo Visio antes de abrirlo porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.
### **Ejemplo de programación de formato de detección**
El siguiente código de ejemplo ilustra cómo detectar un formato de archivo (usando la ruta del archivo o la secuencia) y verificar su extensión.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **Detectar el formato de un archivo Visio desde un InputStream**
Usando Aspose.Diagram for Java API, los desarrolladores pueden detectar el formato de un archivo Visio pasando un flujo de entrada. El método detectFileFormat de la clase FileFormatUtil se puede usar para lograr esto.
### **Detectar formato de una muestra de programación de InputStream**
El siguiente código de ejemplo ilustra cómo detectar un formato de archivo mediante un flujo de entrada.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
