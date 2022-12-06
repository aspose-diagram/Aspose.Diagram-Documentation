---
title: Aspose.Diagram for .NET 18.10 发行说明
type: docs
weight: 30
url: /zh/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51527|将 VSDM 转换为 SVG 后图像丢失|强化|
|DIAGRAMNET-51532|VSD 到 PDF - 图像的阴影不正确|强化|
|DIAGRAMNET-51536|形状的阴影在 VSDX 到 SVG 转换后被移除|强化|
|DIAGRAMNET-51544|将 VSDM 转换为 SVG 后从文本中删除下划线|强化|
|DIAGRAMNET-51558|为 Shape.ConnectorsType 实现 Getter|强化|
|DIAGRAMNET-51520|VDX 到 HTML - 输出中出现额外的行|漏洞|
|DIAGRAMNET-51521|将 VSD 保存为 VSDX 后，diagram 中的字体会发生变化|漏洞|
|DIAGRAMNET-51523|VSDX 到 SVG - 缺少箭头|漏洞|
|DIAGRAMNET-51524|VSDM 到 SVG - 蓝十字出现在输出文件中|漏洞|
|DIAGRAMNET-51525|决策的形状从菱形变为正方形，而 VSDM 变为 SVG 转换|漏洞|
|DIAGRAMNET-51528|决策的形状从菱形变为正方形，而 VSDM 变为 SVG 转换|漏洞|
|DIAGRAMNET-51529|VSDM 到 SVG - 虚线转换为实线|漏洞|
|DIAGRAMNET-51531|将 VSDX 转换为 SVG 后，形状将移至右侧|漏洞|
|DIAGRAMNET-51533|VISIO 转 SVG 后出现红叉|漏洞|
|DIAGRAMNET-51534|形状左下角出现红点|漏洞|
|DIAGRAMNET-51538|VSDX转PDF后图片丢失|漏洞|
|DIAGRAMNET-51541|将 VSDX 转换为 SVG 后文本不可见|漏洞|
|DIAGRAMNET-51542|文本在 VSDX 到 SVG 转换后被删除|漏洞|
|DIAGRAMNET-51543|时间和日期格式在 VSDM TO SVG 之后更改|漏洞|
|DIAGRAMNET-51545|VSDX 到 SVG - 文本包装在输出中|漏洞|
|DIAGRAMNET-51546|VSDX 到 SVG - 文本包装在输出中|漏洞|
|DIAGRAMNET-51547|VSDX 到 SVG - 文本包装在输出中|漏洞|
|DIAGRAMNET-51548|VSDX 到 SVG - 文本包装在输出中|漏洞|
|DIAGRAMNET-51551|无法获得正确的形状主题颜色|漏洞|
|DIAGRAMNET-51552|SVG 转换中显示的反向箭头|漏洞|
|DIAGRAMNET-51559|将 VSDM 转换为 SVG 时出现文本大小调整问题|漏洞|
|DIAGRAMNET-51560|转换为 SVG 后连接线变细|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
#### **在 Shape 中添加 InheritLine**
包含由父样式和主控形状继承的形状的线条格式值。

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **在形状中添加了 GetConnectorsType**
获取连接器类型

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

