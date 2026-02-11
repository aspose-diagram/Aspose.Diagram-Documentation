---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /python-java/your-first-aspose-diagram-application-hello-world/
description: This page describes how to create first application with Aspose.Diagram library.
---

{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. Create an instance of the Diagram class.
1. Apply the license:
   1. If you have purchased a license, then use the license in your application to get access to Aspose.Diagram' full functionality
   1. If you are using the evaluation version of the component (if you're using Aspose.Diagram without a license), skip this step.
1. Create a new Visio file, or open an existing Visio file.
1. Create a new text box.
1. Insert the words **Hello World!** into a text box.
1. Generate the modified Microsoft Visio file.

The implementation of the above steps is demonstrated in the examples below.

### **Code Sample: Creating a New Diagram and Writing Hello World!**

The following example opens an existing Microsoft Visio template file named "[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.

```
{{< highlight "python" >}}
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
```
