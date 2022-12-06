---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /es/net/your-first-aspose-diagram-application-hello-world/
description: Esta página describe cómo crear la primera aplicación con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) clase.
1.  Si tiene una licencia, entonces[apliquelo](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Si está utilizando la versión de evaluación, omita las líneas de código relacionadas con la licencia.
1. Cree un nuevo archivo Visio o abra un archivo Visio existente.
1. Crear un nuevo cuadro de texto.
1.  Inserta las palabras**Hello World!** en un cuadro de texto.
1. Genere el archivo Microsoft Visio modificado.

La implementación de los pasos anteriores se demuestra en los siguientes ejemplos.

### **Ejemplo de código: creación de un nuevo Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateNewVisio-CreateNewVisio.cs" >}}

### **Ejemplo de código: abrir un archivo existente**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ReadVisioDiagram-ReadVisioDiagram.cs" >}}
