---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /zh/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

This beginner's topic shows how developers can create a simple first application (Hello World) using Aspose.Diagram' simple API. The application creates a Microsoft Visio file with the words Hello World in the page.

{{% /alert %}}

### **Creating the Hello World Application**

To create the Hello World application using Aspose.Diagram API:

1. 创建工作簿类的实例。
1. 申请许可证：
 1. 如果您购买了许可证，则在您的应用程序中使用该许可证来访问 Aspose.Diagram 的全部功能
1. 如果您使用的是组件的评估版（如果您使用的是 Aspose.Diagram 无许可证），请跳过此步骤。
1. 创建一个新的 Microsoft Visio 文件，或打开一个现有文件，您要在其中添加/更新一些文本。
1. 插入单词**Hello World!**进入访问的页面。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤。

#### **创建一个 Diagram**

The following example creates a new diagram from scratch, writes the words "Hello World!" on the first page, and saves the file.

**创建新的 visio 文件** 

![待办事项：图片_替代_文本](your-first-aspose-diagram-application-hello-world_1.png)


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


#### **打开现有文件**

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

