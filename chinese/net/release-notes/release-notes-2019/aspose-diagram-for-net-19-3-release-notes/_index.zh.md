---
title: Aspose.Diagram for .NET 19.3 发行说明
type: docs
weight: 100
url: /zh/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50930|添加对在操作系统上检索常用字体目录的支持|强化|
|DIAGRAMNET-51614|获取 Shape 的所有 Props 值|强化|
|DIAGRAMNET-50214|VSD 到PDF转换-曲线变成直线|漏洞|
|DIAGRAMNET-50240|VSD 到 PDF 转换 - 动态连接器布局错误|漏洞|
|DIAGRAMNET-50703|VSDX 到 PDF 导出 - 缺少动态连接器|漏洞|
|DIAGRAMNET-50704|VSD 到 PDF 导出 - 元类型形状变成混乱的符号|漏洞|
|DIAGRAMNET-51535|VSDM 到 SVG - SVG 中的字体从 Sans 更改为 Serif|漏洞|
|DIAGRAMNET-51574|VSDX 到 PNG - 某些形状在输出 PNG 中呈现不正确|漏洞|
|DIAGRAMNET-51608|文本换行未按预期工作|漏洞|
|DIAGRAMNET-51609|将 Diagram 复制到 PowerPoint 幻灯片时，形状向左侧移动|漏洞|
|DIAGRAMNET-51617|Visio 到 PDF - 外部数据驱动值未正确显示|漏洞|
|DIAGRAMNET-51619|Visio 到 PDF - PDF 中的日期/时间/距离不正确|漏洞|
|DIAGRAMNET-51621|Visio 到 PDF - 背景图像失真并且 PDF 中存在额外页面|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Diagram 中添加 GetDefaultFontDir**
获取默认字体文件夹路径

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
