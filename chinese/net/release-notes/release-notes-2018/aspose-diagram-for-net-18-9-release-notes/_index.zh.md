---
title: Aspose.Diagram for .NET 18.9 发行说明
type: docs
weight: 40
url: /zh/net/aspose-diagram-for-net-18-9-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 18.9](https://www.nuget.org/packages/Aspose.Diagram/18.9.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51509|VSDX 到 PNG - 输出图像中的线条不透明度丢失|强化|
|DIAGRAMNET-51510|VSDX 到 SVG - 输出图像中的线条不透明度丢失|强化|
|DIAGRAMNET-51516|将多个 VISIO 文件合并为单个输出|强化|
|DIAGRAMNET-50272|VSD 到 SVG 转换 - 一些连接点的位置和大小错误|漏洞|
|DIAGRAMNET-50273|VSD 到 SVG - 形状文本项的对齐方式不正确|漏洞|
|DIAGRAMNET-50487|VSD 到 HTML - 值之间的斜杠字符错位|漏洞|
|DIAGRAMNET-50975|VSDX 到 PDF - 形状的背景颜色为黑色|漏洞|
|DIAGRAMNET-50976|VSDX 到 HTML - 形状的背景颜色为黑色|漏洞|
|DIAGRAMNET-50980|VSDX 到 PNG - 菱形内的数字错位|漏洞|
|DIAGRAMNET-51129|将 VSD 转换为 PDF 时文本项未正确对齐|漏洞|
|DIAGRAMNET-51511|PNG 转换中的附加箭头|漏洞|
|DIAGRAMNET-51512|SVG 转换中显示的附加箭头|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
#### **在 Diagram 类中添加了 Combine 方法**
将一个 Diagram 对象与另一个 Diagram 对象组合。

{{< highlight "java" >}}

             Diagram diagramF = new Diagram( "f.vsdx");

            Diagram diagramS = new Diagram( "s.vsdx");

            diagramF.Combine(diagramS);

{{< /highlight >}}
