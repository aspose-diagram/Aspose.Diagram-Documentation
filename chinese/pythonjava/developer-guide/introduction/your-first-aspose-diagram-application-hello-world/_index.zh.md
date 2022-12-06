---
title: 您的第一个 Aspose.Diagram 应用程序 - Hello World
type: docs
weight: 30
url: /zh/python-java/your-first-aspose-diagram-application-hello-world/
description: 本页介绍如何使用 Aspose.Diagram 库创建第一个应用程序。
---
{{% alert color="primary" %}}

本教程介绍如何使用 Aspose.Diagram' 简单 API 创建第一个应用程序 (Hello World)。这个简单的应用程序在指定页面中创建一个 Microsoft Visio 文件，其中包含文本“Hello World”。

{{% /alert %}}

## **创建 Hello World 应用程序**

以下步骤使用 Aspose.Diagram API 创建 Hello World 应用程序：

1. 创建 Diagram 类的实例。
1. 申请许可证：
 1. 如果您购买了许可证，则在您的应用程序中使用该许可证来访问 Aspose.Diagram 的全部功能
1. 如果您使用的是组件的评估版（如果您使用的是 Aspose.Diagram 无许可证），请跳过此步骤。
1. 创建一个新的 Visio 文件，或打开一个现有的 Visio 文件。
1. 创建一个新的文本框。
1. 插入单词**你好世界！**到一个文本框中。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤的实现。

### **代码示例：创建一个新的 Diagram 并编写 Hello World！**

以下示例打开一个名为“Microsoft Visio”的模板文件[Basic_Shapes.vss](Basic_Shapes.vss)"，在第一页输入"Hello World!"文本，保存diagram。

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-CreatingHelloWorldVisioFile.py" >}}
