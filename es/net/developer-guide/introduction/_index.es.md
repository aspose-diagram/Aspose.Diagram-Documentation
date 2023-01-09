---
title: Introducción
type: docs
weight: 10
url: /es/net/introduction/
description: Introducción de la biblioteca Aspose.Diagram.
---
## **Obtenga la información del documento Visio de la biblioteca Aspose.Diagram for .NET**
Microsoft Visio guarda información sobre las acciones realizadas en un diagram dentro del archivo. Por ejemplo, la hora y la fecha en que se creó el documento, la última vez que se editó, imprimió o guardó, se guardan con el archivo. También se guarda información sobre qué versión de Microsoft Visio creó y editó por última vez el archivo.

Este artículo explica cómo recuperar esa información.
### **Determinar la versión de Microsoft Visio que creó, editó y guardó un documento**
 La propiedad Version expuesta por el[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)La clase y la propiedad BuildNumberCreated expuesta por la clase DocumentProperties se utilizan para determinar la versión y el número de compilación completo de la instancia Microsoft Visio utilizada para crear el documento.

 La propiedad BuildNumberEdited expuesta por el[Propiedades del documento](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) class se utiliza para determinar el número de compilación completo de la instancia Microsoft Visio utilizada para editar el documento.

Las propiedades TimeCreated, TimeEdited, TimePrinted y TimeSaved expuestas por la clase DocumentProperties se utilizan para determinar la hora en que se creó, se editó por última vez, se imprimió por última vez y se guardó por última vez el documento Microsoft Visio.

También puede configurar estas propiedades para cambiar la información en el archivo. Los ejemplos de código a continuación muestran cómo recuperar información sobre qué creó el archivo, así como cuándo se creó, editó, imprimió y guardó.
#### **Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Escritura Visio Resumen del documento Información**
Microsoft Visio le permite definir una serie de propiedades de información de resumen del documento para ayudarlo a usted y a sus colegas a identificar un diagram. Las propiedades de resumen, por ejemplo, título, tema, autor y descripción, hacen que el archivo sea más fácil de encontrar al buscar y más fácil de reconocer cuando exploración de archivos.
### **Escritura Microsoft Visio Resumen del documento Información**
La clase DocumentProperties expone una serie de propiedades para establecer u obtener información de resumen de Microsoft Visio diagram. Aspose.Diagram for .NET puede actualizar la información de resumen del dibujo y luego volver a escribir el archivo de dibujo en VDX.

{{% alert color="primary" %}} 

Tenga en cuenta que no puede establecer valores contra el**Solicitud**y**Productor**porque Aspose Ltd. y Aspose.Diagram for .NET xxx se mostrarán en estos campos.

{{% /alert %}} 

Para actualizar la información de resumen del dibujo de un archivo VDX o VSD existente:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) clase.
1.  Establecer propiedades expuestas por[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) para definir la información de resumen para el archivo de dibujo Visio.
1. Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VDX.

Consulta la información resumida:

1. Abra el archivo de salida VDX en Microsoft Visio.
1. Seleccionando Información en el menú Archivo.
#### **Escritura Visio Documento Resumen Información Programación Muestra**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Detectar el formato del archivo Visio**
Usando Aspose.Diagram for .NET API, los desarrolladores pueden detectar el formato del archivo Visio antes de abrirlo porque la extensión del archivo no garantiza que el contenido del archivo sea apropiado.
### **Ejemplo de programación de formato de detección**
El siguiente código de ejemplo ilustra cómo detectar un formato de archivo (usando la ruta del archivo o la secuencia) y verificar su extensión.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
