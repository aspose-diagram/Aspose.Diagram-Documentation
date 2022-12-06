---
title: Aspose.Diagram for .NET 20.1 发行说明
type: docs
weight: 70
url: /zh/net/aspose-diagram-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 20.1 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51198|将 VSDM 保存到 SVG 时，超链接按钮上的阴影未正确呈现|强化|
|DIAGRAMNET-51526|VSDX 到 PDF - 箭头的渐变填充在生成的 PDF 中丢失|强化|
|DIAGRAMNET-51539|形状渐变在输出 SVG 中丢失|强化|
|DIAGRAMNET-50705|VSD 到 SVG 导出 - 元类型形状变成混乱的符号|漏洞|
|DIAGRAMNET-51664|删除未使用的主题后文件损坏|漏洞|
|DIAGRAMNET-51665|删除未使用的主题后图像显示为 X|漏洞|
|DIAGRAMNET-51684|删除未使用的主形状和样式时，只有图像有问题|漏洞|
|DIAGRAMNET-51726|背景图像缺失（PowerPoint 已添加到 VISIO 中）同时删除未使用的主控形状和样式|漏洞|
|DIAGRAMNET-51737|Visio 到 Html - 图片大小问题|漏洞|
|DIAGRAMNET-51743|从 Visio 中删除私人信息 - Visio 文档大小问题|漏洞|
|DIAGRAMNET-51745|将 VSD 转换为 VSDX 时 WPF 应用程序中出现奇怪的错误|漏洞|

## **公共 API 和向后不兼容的更改**
- 将页面添加到 LoadOptions - 指定要加载的页面的索引。



{{< highlight "java" >}}

Aspose.Diagram.LoadOptions options = new Aspose.Diagram.LoadOptions(LoadFileFormat.VSDX);

options.Pages = new ArrayList();

options.Pages.Add(0);

{{< /highlight >}}

- 在 FontConfigs 中添加了 SetFontSources - 设置字体源

{{< highlight "java" >}}

Aspose.Diagram.MemoryFontSource sc1 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource sc2 = new Aspose.Diagram.MemoryFontSource(b);

Aspose.Diagram.MemoryFontSource[]sc = new Aspose.Diagram.MemoryFontSource[]{ sc1, sc2 };

Aspose.Diagram.FontConfigs.SetFontSources(sc); 

{{< /highlight >}}
