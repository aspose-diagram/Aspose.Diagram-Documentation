---
title: 您的第一个 Aspose.Diagram 应用程序 - Hello World
type: docs
weight: 30
url: /zh/java/your-first-aspose-diagram-application-hello-world/
description: 本页介绍如何使用 Aspose.Diagram 库创建第一个应用程序。
---
{{% alert color="primary" %}}

本教程介绍如何使用 Aspose.Diagram' 简单 API 创建第一个应用程序 (Hello World)。这个简单的应用程序在指定页面中创建一个 Microsoft Visio 文件，其中包含文本“Hello World”。

{{% /alert %}}

## **创建 Hello World 应用程序**

以下步骤使用 Aspose.Diagram API 创建 Hello World 应用程序：

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)班级。
1. 如果你有驾照，那么[应用它](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
如果您使用的是评估版，请跳过与许可证相关的代码行。
1. 创建一个新的 Visio 文件，或打开一个现有的 Visio 文件。
1. 创建一个新的文本框。
1. 插入单词**你好世界！**到一个文本框中。
1. 生成修改后的 Microsoft Visio 文件。

下面的示例演示了上述步骤的实现。

### **代码示例：创建一个新的 Diagram**

以下示例从头开始创建一个新的 diagram，写为 Hello World！在第一页上并保存 Visio 文件。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-CreateNewVisio-CreateNewVisio.java" >}}

### **代码示例：打开现有文件**

下面的例子打开一个已有的Microsoft Visio模板文件，名称为“Sample.vsdx”，输入“Hello World!”第一页中的文本并保存 diagram。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
