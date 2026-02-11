---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /es/python-java/your-first-aspose-diagram-application-hello-world/
description: Esta página describe cómo crear la primera aplicación con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Cree una instancia de la clase Diagram.
1. Aplicar la licencia:
 1. Si ha comprado una licencia, use la licencia en su aplicación para obtener acceso a la funcionalidad completa de Aspose.Diagram
 1. Si está utilizando la versión de evaluación del componente (si está utilizando Aspose.Diagram sin licencia), omita este paso.
1. Cree un nuevo archivo Visio o abra un archivo Visio existente.
1. Crear un nuevo cuadro de texto.
1.  Inserta las palabras**Hello World!** en un cuadro de texto.
1. Genere el archivo Microsoft Visio modificado.

La implementación de los pasos anteriores se demuestra en los siguientes ejemplos.

### **Code Sample: Creating a New Diagram and Writing Hello World!**

El siguiente ejemplo abre un archivo de plantilla Microsoft Visio existente llamado "[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

diagram = Diagram("Basic_Shapes.vss")

# Add a new hello world rectangle shape
shapeId = diagram.addShape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.getPages().getPage(0).getShapes().getShape(shapeId)
shape.getText().getValue().add(Txt("Hello World"))

# Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

