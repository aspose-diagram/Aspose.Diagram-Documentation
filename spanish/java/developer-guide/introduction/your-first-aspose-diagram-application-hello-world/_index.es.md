---
title: Su primera aplicación Aspose.Diagram - Hola mundo
type: docs
weight: 30
url: /es/java/your-first-aspose-diagram-application-hello-world/
description: Esta página describe cómo crear la primera aplicación con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

Este tutorial muestra cómo crear una primera aplicación (Hello World) usando Aspose.Diagram' simple API. Esta aplicación simple crea un archivo Microsoft Visio con el texto 'Hello World' en una página específica.

{{% /alert %}}

## **Creación de la aplicación Hello World**

Los pasos a continuación crean la aplicación Hello World usando el Aspose.Diagram API:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) clase.
1.  Si tiene una licencia, entonces[apliquelo](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 Si está utilizando la versión de evaluación, omita las líneas de código relacionadas con la licencia.
1. Cree un nuevo archivo Visio o abra un archivo Visio existente.
1. Crear un nuevo cuadro de texto.
1.  Inserta las palabras**Hola Mundo!** en un cuadro de texto.
1. Genere el archivo Microsoft Visio modificado.

La implementación de los pasos anteriores se demuestra en los siguientes ejemplos.

### **Ejemplo de código: creación de un nuevo Diagram**

El siguiente ejemplo crea un nuevo diagram desde cero, escribe Hello World! en la primera página y guarda el archivo Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **Ejemplo de código: abrir un archivo existente**

El siguiente ejemplo abre un archivo de plantilla Microsoft Visio existente llamado "Sample.vsdx", ingresa "Hello World!" texto en la primera página y guarda el diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
