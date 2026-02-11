---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /zh/python-java/your-first-aspose-diagram-application-hello-world/
description: 本页介绍如何使用 Aspose.Diagram 库创建第一个应用程序。
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1. 创建 Diagram 类的实例。
1. 申请许可证：
 1. 如果您购买了许可证，则在您的应用程序中使用该许可证来访问 Aspose.Diagram 的全部功能
1. 如果您使用的是组件的评估版（如果您使用的是 Aspose.Diagram 无许可证），请跳过此步骤。
1. 创建一个新的 Visio 文件，或打开一个现有的 Visio 文件。
1. 创建一个新的文本框。
1. 插入单词**Hello World!**到一个文本框中。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤的实现。

### **Code Sample: Creating a New Diagram and Writing Hello World!**

以下示例打开一个名为“Microsoft Visio”的模板文件[Basic_Shapes.vss](Basic_Shapes.vss)", inputs "Hello World!" text in the first page and saves the diagram.


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

