---
title: 您的第一个 Aspose.Diagram 应用程序 - Hello World
type: docs
weight: 30
url: /zh/python-net/your-first-aspose-diagram-application-hello-world/
---
{{% alert color="primary" %}}

这个初学者主题展示了开发人员如何使用 Aspose.Diagram' simple API 创建一个简单的第一个应用程序 (Hello World)。该应用程序创建一个 Microsoft Visio 文件，页面中包含 Hello World 字样。

{{% /alert %}}

### **创建 Hello World 应用程序**

使用 Aspose.Diagram API 创建 Hello World 应用程序：

1. 创建工作簿类的实例。
1. 申请许可证：
 1. 如果您购买了许可证，则在您的应用程序中使用该许可证来访问 Aspose.Diagram 的全部功能
1. 如果您使用的是组件的评估版（如果您使用的是 Aspose.Diagram 无许可证），请跳过此步骤。
1. 创建一个新的 Microsoft Visio 文件，或打开一个现有文件，您要在其中添加/更新一些文本。
1. 插入单词**你好世界！**进入访问的页面。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤。

#### **创建一个 Diagram**

下面的示例从头开始创建一个新的 diagram，写下“Hello World!”在第一页上，并保存文件。

**创建新的 visio 文件** 

![待办事项：图片_替代_文本](your-first-aspose-diagram-application-hello-world_1.png)

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingNewVisioFile.py" >}}

#### **打开现有文件**

下面的例子打开一个已有的 Microsoft Visio 模板文件，写入文字“Hello World!”在第一页，并将 diagram 另存为新文件。

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-CreatingHelloWorldVisioFile.py" >}}
