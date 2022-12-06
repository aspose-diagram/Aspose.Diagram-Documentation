---
title: 管理文档属性
linktitle: 文档属性
type: docs
weight: 80
url: /zh/net/document-properties/
aliases: [/net/document-properties/]
description: 管理 visio 文件的文档属性。
---
## **介绍**

Microsoft Visio 提供向 visio 文件添加属性的功能。这些文档属性提供了有用的信息，分为 2 个类别，详述如下。

- 系统定义（内置）属性：内置属性包含有关文档的一般信息，如文档标题、作者姓名、文档统计信息等。
- 用户定义（自定义）属性：最终用户以名称-值对的形式定义的自定义属性。

{{% alert color="primary" %}}

关于内置属性和自定义属性最重要的一点是内置属性可以访问和修改，但不能创建或删除。但是，可以创建和管理自定义属性。

{{% /alert %}}

## **使用 Microsoft Visio 管理文档属性**

Microsoft Visio 允许您以所见即所得的方式管理Visio文件的文档属性。请按照以下步骤打开**特性**Visio 2016 中的对话框。

1. 来自**文件**菜单，选择**信息**.

|**选择信息菜单**|
|:- |
|![待办事项：图片_替代_文本](managing-document-properties_1.png)|
1. 点击**特性**标题并选择“高级属性”。

|**单击高级属性选择**|
|:- |
|![待办事项：图片_替代_文本](managing-document-properties_2.png)|
1. 管理文件的文档属性。

|**属性对话框**|
|:- |
|![待办事项：图片_替代_文本](managing-document-properties_3.png)|
在 Properties 对话框中，有不同的选项卡，如 General、Summary、Statistics、Contents 和 Customs。每个选项卡都有助于配置与文件相关的不同类型的信息。自定义选项卡用于管理自定义属性。

## **使用 Aspose.Diagram 处理文档属性**

开发人员可以使用 Aspose.Diagram API 动态管理文档属性。此功能可帮助开发人员将有用的信息与文件一起存储，例如文件的接收、处理时间、时间戳等。

{{% alert color="primary" %}}

Aspose.Diagram for .NET 直接在输出文件中写入API和Version Number的信息。

请注意，您不能指示 Aspose.Diagram for .NET 更改或从输出文档中删除此信息。

{{% /alert %}}

### **访问文档属性**

Aspose.Diagram API 支持两种类型的文档属性，内置的和自定义的。 Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram) class 代表一个 Visio 文件，和 visio 文件一样，[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)类可以包含多个页面，每个页面由[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page)类，而页面集合由[**页面集合**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)班级。

使用[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/Diagram)访问文件的文档属性，如下所述。

- 要访问内置文档属性，请使用[**diagram.DocumentProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties).
- 要访问自定义文档属性，请使用[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties/properties/customprops).

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AccessingDocumentProperties.cs" >}}

### **添加或删除自定义文档属性**

正如我们之前在本主题开头所述，开发人员无法添加或删除内置属性，因为这些属性是系统定义的，但可以添加或删除自定义属性，因为它们是用户定义的。

### **添加自定义属性**

Aspose.Diagram API暴露了[**添加**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/add)的方法[**自定义道具集合**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection)类以便将自定义属性添加到集合中。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AddingCustomProperties.cs" >}}

### **删除自定义属性**

要使用 Aspose.Diagram 删除自定义属性，请调用[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/net/aspose.diagram/custompropcollection/methods/remove)方法并传递要删除的文档属性的名称。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemovingCustomProperties.cs" >}}
