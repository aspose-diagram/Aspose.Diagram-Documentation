---
title: 检索 Visio 连接器和字体信息
type: docs
weight: 20
url: /zh/net/retrieve-visio-connectors-and-font-information/
description: 本节介绍如何获取 visio 连接器和字体信息。
---
## **检索连接器信息**
Aspose.Diagram for .NET 提供检索信息的机制 - ID 和名称 - 关于[页数](/diagram/zh/net/retrieve-2c-get-2c-copy-and-insert-a-page/)和[掌握](https://docs.aspose.com/diagram/net/working-with-masters/).它还可以让您获得有关连接器（连接形状的元素）的信息。

这[连接](http://www.aspose.com/api/net/diagram/aspose.diagram/connect)对象表示连接 Visio 绘图页上两个形状的连接器。 Connects 属性，由[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类支持 Aspose.Diagram.Connect 对象的集合。此属性可用于检索有关连接器的 ID 和名称信息。
### **编程范例**
以下代码段检索 diagram 中连接器的信息。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.cs" >}}
## **检索字体信息**
Aspose.Diagram 具有从中检索有关构成 diagram 的元素的信息的机制[页数](/diagram/zh/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [模版](https://docs.aspose.com/diagram/net/working-with-masters/), [连接器](/diagram/zh/net/retrieving-connector-information/)还有字体。本文介绍如何找出 diagram 中使用了哪些字体。

这[字体](http://www.aspose.com/api/net/diagram/aspose.diagram/font)对象表示应用于文档中的文本或可在系统上使用的字体。字体对象将名称（例如“Arial”）映射到字体 ID（例如 3），字体 ID Microsoft Visio 存储在形状的字符部分的字体单元格中，该形状包含使用该字体设置格式的文本。当在不同系统上打开文档或安装或删除字体时，字体 ID 可能会发生变化。
### **检索字体编程示例**
下面这段代码从 Visio diagram 中检索字体信息。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveFontInfo-RetrieveFontInfo.cs" >}}
### **获取默认字体目录**
Aspose.Diagram for .NET API 还允许使用 Diagram 类的 GetDefaultFontDir() 方法获取默认字体目录路径。以下代码从 Visio diagram 中检索默认字体目录。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.cs" >}}
### **获取未使用的字体**
{{% alert color="primary" %}}

版本 19.6 或更高版本支持此方法。

{{% /alert %}}

Aspose.Diagram for .NET API 还允许使用 Diagram 类的 GetUnusedStyles() 方法获取未使用的字体。下面的一段代码从 Visio diagram 中检索未使用的字体。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetUnusedFonts-1.cs" >}}
