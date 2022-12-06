---
title: Aspose.Diagram for .NET 22.4 发行说明
type: docs
weight: 24
url: /zh/net/aspose-diagram-for-net-22-4-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 22.4 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-52015|#DIAGRAMNET-51995 的续票 - Aspose.Diagram 文件和 Skyline Datamine 的问题|强化|
|DIAGRAMNET-52707|对形状表公式/值的更改不会触发相关单元格中的更改|强化|
|DIAGRAMNET-50345|VSDX 到 PDF 转换，形状的背景颜色不正确|漏洞|
|DIAGRAMNET-50954|将 VSDX 转换为 PNG 时呈现表格和单选按钮的格式问题|漏洞|
|DIAGRAMNET-52708|文本位置转换为 svg|漏洞|
|DIAGRAMNET-52739|文化敏感点格式|漏洞|
|DIAGRAMNET-52759|将 .vsdx 文件转换为 pdf 时，表中的文本被删除|漏洞|
|DIAGRAMNET-52762|VSDX 到 PDF - 图片未转换|漏洞|
|DIAGRAMNET-52779|将 Visio 转换为 SVG 时椭圆不缩放|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。
### **在形状中添加 GetPureText**
- 获取形状的文本字符串。

{{< highlight "java" >}}
String text = shape.GetPureText();
{{< /highlight >}}

