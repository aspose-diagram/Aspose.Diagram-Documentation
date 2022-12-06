---
title: Aspose.Diagram for .NET 19.5 发行说明
type: docs
weight: 80
url: /zh/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51606|从 Visio 图中检测并删除未使用的主题、数据图形和样式|强化|
|DIAGRAMNET-51637|分组容器内的嵌套形状未正确保留|强化|
|DIAGRAMNET-51638|当值为整数时无法获取 Prop.Value.Val|强化|
|DIAGRAMNET-51640|确定 Visio 文件中未使用的样式|强化|
|DIAGRAMNET-50051|VSDX 到 PDF 转换，缺少连接箭头以及放错位置的文本|漏洞|
|DIAGRAMNET-50052|VSDX 到 PDF 转换，字体文本颜色不正确的形状|漏洞|
|DIAGRAMNET-51179|将 VSDM 转换为 SVG 时电子邮件按钮上的阴影不正确|漏洞|
|DIAGRAMNET-51190|将 VDX 保存到 SVG 时超链接形状显示不正确|漏洞|
|DIAGRAMNET-51194|将 VDX 保存为 SVG 时图标呈现不正确|漏洞|
|DIAGRAMNET-51254|将 VSDM 转换为 SVG 时顶部栏中的阴影不正确|漏洞|
|DIAGRAMNET-51618|Visio 到 PDF - 错误的日期格式和缺失的数据|漏洞|
|DIAGRAMNET-51628|.vsdx 图表中已删除默认文本的文本值不正确|漏洞|
|DIAGRAMNET-51634|Visio 到 SVG - 输出中某些形状的 z-index 错误|漏洞|
|DIAGRAMNET-51636|Visio 到 SVG - 并非所有路径元素都正确导出为矩形元素|漏洞|
|DIAGRAMNET-51641|使用 API 重新保存 Visio 时会显示额外的图像|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Diagram 中添加 GetUnusedStyles**
获取未使用的样式。

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
