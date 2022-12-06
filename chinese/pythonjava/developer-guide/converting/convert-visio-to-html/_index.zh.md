---
title: 将 Visio 转换为 HTML 格式
linktitle: 将 Visio 转换为 HTML
type: docs
weight: 30
url: /zh/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **将 Visio 导出为 HTML** ##
本文介绍了如何使用 将 Microsoft Visio diagram 导出到 HTML[Aspose.Diagram 为 Python 通过 Java](https://products.aspose.com/diagram/python-java/) API.

使用 Diagram 类构造函数读取 diagram 文件，并使用 Save 方法将 diagram 导出为任何支持的图像格式。开发人员可以将生成的 HTML 保存在本地存储中或直接保存到流实例中。

下图显示了一个[VSD档案](ExportToHTML.vsd)即将保存为 PNG 格式。您也可以使用其他 diagram 格式（VSDX、VSTM、VSTM、VSSX、VSS、VSSM、VDX、VST、VSTX、VDX、VTX 或 076110）

**输入 diagram。**

![待办事项：图片_替代_文本](http://i.imgur.com/YX4BNNq.png)

为了将 VSD diagram 导出为 HTML，请执行以下步骤：

1. 创建 Diagram 类的实例。
1. 调用 Dagram 类的 Save 方法并将 HTML 设置为输出格式。

下图显示了输出的 HTML 文件。

**输出 HTML diagram。**

![待办事项：图片_替代_文本](http://i.imgur.com/syavUqI.png)

### **将生成的 HTML 保存在本地存储中**
生成的文件可以通过传递完整的路径字符串来保存，包括文件名和扩展名，例如@"c:\temp\MyOutput.html"。

#### **将生成的 HTML 保存在本地存储编程示例中**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **将生成的 HTML 保存在流实例中**
它适用于将生成的 HTML 保存在数据库或存储库中而不将其存储在本地存储中的用例。此功能还嵌入了 HTML 的其他结果资源，例如字体、CSS（包含样式信息）和图像。因为它将单个 HTML 文件保存到流实例中。
#### **将生成的 HTML 保存在流编程示例中**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
