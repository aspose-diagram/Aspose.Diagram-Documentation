---
title: Aspose.Diagram for .NET 19.9 发行说明
type: docs
weight: 40
url: /zh/net/aspose-diagram-for-net-19-9-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 19.9 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51683|Visio 到 HTML - 生成的 HTML 中的链接无法正常工作|强化|
|DIAGRAMNET-51684|删除未使用的主形状和样式时，只有图像有问题|强化|
|DIAGRAMNET-51711|转换后无法添加宏|强化|
|DIAGRAMNET-50383|缩小 Visio diagram 的大小|漏洞|
|DIAGRAMNET-51682|从 Diagram 获取字体样式|漏洞|
|DIAGRAMNET-51685|Visio 到 SVG - 发生异常|漏洞|
|DIAGRAMNET-51686|Visio 到 PNG - 输出文件包含不需要的图像和形状|漏洞|
|DIAGRAMNET-51687|Visio 到 PDF - 输出 PDF 中缺少文本背景色|漏洞|
|DIAGRAMNET-51688|Visio 到 PDF - 形状框的颜色在输出中不同|漏洞|
|DIAGRAMNET-51689|Visio 到 JPG - 输出图像格式不正确|漏洞|
|DIAGRAMNET-51691|Visio 到 PDF - 有些形状不正确|漏洞|
|DIAGRAMNET-51692|Visio 到 PDF - 有些形状不正确|漏洞|
|DIAGRAMNET-51693|Visio 到 PDF - 有些形状不正确|漏洞|
|DIAGRAMNET-51694|Visio 到 PDF - 有些形状不正确|漏洞|
|DIAGRAMNET-51697|Visio 到 PDF - 有些形状不正确|漏洞|
|DIAGRAMNET-51700|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51702|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51706|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51707|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51708|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51709|Visio 到 PDF - 一些形状/线条不正确|漏洞|
|DIAGRAMNET-51710|Visio 到 PDF - 一些形状/线条不正确|漏洞|
### **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。

|**改变**|**目的**|**样本**|
|:- |:- |:- |
|外加的**加粗**到 Aspose.Shape.Char|指示字体是否为粗体。|<p>Aspose.Diagram.Char ch = shape.Chars[0];</p><p>ch.IsBold</p>|
|外加的**斜体**到 Aspose.Shape.Char|指示字体是否为斜体。|<p>Aspose.Diagram.Char ch = shape.Chars[0];</p><p>ch.IsItalic</p>|
|外加的**是下划线**到 Aspose.Shape.Char|指示字体是否为下划线。|<p>Aspose.Diagram.Char ch = shape.Chars[0];</p><p>ch.IsUnderline</p>|
|外加的**是双下划线**到 Aspose.Shape.Char|指示字体是否为双下划线|<p>Aspose.Diagram.Char ch = shape.Chars[0];</p><p>ch.IsDoubleUnderline</p>|
|外加的**是删除线**到 Aspose.Shape.Char|指示字体是否有删除线。|<p>Aspose.Diagram.Char ch = shape.Chars[0]</p><p>ch.是删除线</p>|
|外加的**是双删除线**到 Aspose.Shape.Char|指示字体是否为双删除线|<p>Aspose.Diagram.Char ch = shape.Chars[0];</p><p>ch.IsDoubleStrikethrough</p>|

