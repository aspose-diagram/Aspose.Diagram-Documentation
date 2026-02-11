---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /es/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. Cree una instancia de la clase Workbook.
1. Aplicar la licencia:
 1. Si ha comprado una licencia, use la licencia en su aplicación para obtener acceso a la funcionalidad completa de Aspose.Diagram
 1. Si está utilizando la versión de evaluación del componente (si está utilizando Aspose.Diagram sin licencia), omita este paso.
1. Cree un nuevo archivo Microsoft Visio o abra un archivo existente en el que desee agregar/actualizar algún texto.
1.  Inserta las palabras**Hello World!** en la página accedida.
1. Genere el archivo Microsoft Visio modificado.

Los siguientes ejemplos demuestran los pasos anteriores.

#### **Creando un Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**Crear nuevo archivo visio** 

![todo:imagen_alternativa_texto](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **Abrir un archivo existente**

The following example opens an existing Microsoft Visio template file, writes the words "Hello World!" in the first page, and saves the diagram as a new file.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

diagram = Diagram(os.path.join(sourceDir, "Basic Shapes.vss"))

#// Add a new hello world rectangle shape
shapeId = diagram.add_shape(4.25, 5.5, 2, 1, "Rectangle", 0)
shape = diagram.pages[0].shapes.get_shape(shapeId)
shape.text.value.add(Txt("Hello World"))

#// Save diagram in the VSDX format
diagram.save("CreateHelloWorldVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}

