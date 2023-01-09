﻿---
title: 介绍
type: docs
weight: 10
url: /zh/net/introduction/
description: Aspose.Diagram图书馆介绍。
---
## **获取Aspose.Diagram for .NET图书馆的Visio文献信息**
Microsoft Visio 将有关对 diagram 采取的操作的信息保存在文件中。例如，文档创建的时间和日期，最后一次编辑、打印或保存的时间，都与文件一起保存。有关 Microsoft Visio 创建和最后编辑文件的版本的信息也被保存。

本文介绍了如何检索该信息。
### **Determining the Version of Microsoft Visio 创建、编辑和保存文档**
暴露的 Version 属性[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)类和 DocumentProperties 类公开的 BuildNumberCreated 属性用于确定用于创建文档的 Microsoft Visio 实例的版本和完整构建号。

公开的 BuildNumberEdited 属性[文档属性](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)类用于确定用于编辑文档的 Microsoft Visio 实例的完整构建号。

DocumentProperties 类公开的 TimeCreated、TimeEdited、TimePrinted 和 TimeSaved 属性用于确定 Microsoft Visio 文档的创建、最后编辑、最后打印和最后保存的时间。

您还可以设置这些属性来更改文件中的信息。下面的代码示例显示了如何检索有关文件创建者以及文件创建、编辑、打印和保存时间的信息。
#### **编程范例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **编写 Visio 文档摘要信息**
Microsoft Visio 允许您定义许多文档摘要信息属性，以帮助您和您的同事识别 diagram。摘要属性，例如标题、主题、作者和描述，使文件在搜索时更容易找到，并且在搜索时更容易识别浏览文件。
### **写作 Microsoft Visio 文档摘要信息**
DocumentProperties 类公开了一些属性来设置或获取 Microsoft Visio diagram 的摘要信息。 Aspose.Diagram for .NET 可以更新图纸汇总信息，然后将图纸文件写回VDX。

{{% alert color="primary" %}} 

请注意，您不能针对**应用**和**制作人**字段，因为 Aspose Ltd. 和 Aspose.Diagram for .NET xxx 将针对这些字段显示。

{{% /alert %}} 

要更新现有 VDX 或 VSD 文件的图纸摘要信息：

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)班级。
1. 设置暴露的属性[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops)定义 Visio 图形文件的摘要信息。
1. 调用Diagram类的Save方法将Visio绘图文件写入VDX。

查看摘要信息：

1. 在Microsoft Visio打开输出VDX文件。
1. 从文件菜单中选择信息。
#### **编写 Visio 文档摘要信息编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **检测Visio文件格式**
使用Aspose.Diagram for .NET API，开发者可以在打开Visio文件之前检测其格式，因为文件扩展名并不能保证文件内容是合适的。
### **检测格式编程示例**
以下示例代码说明了如何检测文件格式（使用文件路径或流）并检查其扩展名。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
