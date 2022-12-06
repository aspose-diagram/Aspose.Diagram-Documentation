---
title: Aspose.Diagram for .NET 20.5 发行说明
type: docs
weight: 30
url: /zh/net/aspose-diagram-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 20.5 的发行说明信息。

{{% /alert %}} 
## **改进和变化**
VSD 到 PDF 转换，不保留形状的正确文本对齐方式

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51088|检索 VSD 的错误页数|强化|
|DIAGRAMNET-51731|确定一个形状是否与 diagram 中的另一个形状相交|强化|
|DIAGRAMNET-51833|Aspose.Diagram 20.4: Visio 不支持文档版本|强化|
|DIAGRAMNET-50361|VSD 到 PDF 转换，不保留形状的正确文本对齐方式|漏洞|
|DIAGRAMNET-50955|将 VSDX 转换为 PNG 时，菱形的文本项会发生位移|漏洞|
|DIAGRAMNET-50990|另外，负号和美元符号在将 VSDX 转换为 PNG 时未正确对齐|漏洞|
|DIAGRAMNET-51815|形状中的大量文本行可能会在底部产生明显的位移|漏洞|
|DIAGRAMNET-51820|评估水印不适合页面|漏洞|
|DIAGRAMNET-51821|Visio 到 Html - 输出中的图像和链接问题|漏洞|
|DIAGRAMNET-51823|同时将 Visio 转换为 SVG。一些图像有问题图标丢失|漏洞|
|DIAGRAMNET-51824|同时将 Visio 转换为 SVG。内容对齐错误|漏洞|
|DIAGRAMNET-51826|同时将 Visio 转换为 SVG。图标丢失|漏洞|
|DIAGRAMNET-51827|将 Visio 转换为 SVG 时 - QR 码丢失|漏洞|
|DIAGRAMNET-51828|将 Visio 转换为 SVG 时 - PDF 图标丢失|漏洞|
|DIAGRAMNET-51829|将 Visio 转换为 SVG 时 - 图标丢失（丢失）|漏洞|
|DIAGRAMNET-51830|将 Visio 转换为 SVG 时 - 图像丢失（丢失）|漏洞|
|DIAGRAMNET-51831|Visio 到 HTML - 输出中的图像和链接问题|漏洞|
|DIAGRAMNET-51834|Visio 保存 HTML - 错误的连接器|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。
### **在形状中添加 IsIntersect**
- 指示此形状是否与另一个形状相交。

{{< highlight "java" >}}

Shape s1 = diagram.Pages[0].Shapes.GetShape(1);

Shape s2 = diagram.Pages[0].Shapes.GetShape(2);

bool isIntersect = s1.IsIntersect(s2);

{{< /highlight >}}



