---
title: Aspose.Diagram for .NET 20.8 发行说明
type: docs
weight: 14
url: /zh/net/aspose-diagram-for-net-20-8-release-notes/
---
{{% alert color="primary" %}}

此页面包含 Aspose.Diagram for .NET 20.8 的发行说明信息。

{{% /alert %}}
## **改进和变化**  ##

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51886|创建将 Ole 对象（如单词、单元格、幻灯片等）插入到 Diagram 的单个形状中的能力，其中包含对象数据和预览图像。|强化|
|DIAGRAMNET-51888|Visio 到 PDF - API 需要很长时间才能转换|强化|
|DIAGRAMNET-51889|循环保存到 pdf 超过 20 分钟|强化|
|DIAGRAMNET-51893|VSDX 到 SVG 转换后缺少 viewBox 属性|强化|
|DIAGRAMNET-51851|VSDX 到 PDF - 一些图标丢失，一些未正确呈现|漏洞|
|DIAGRAMNET-51873|VSDX 到 PDF - 内容在输出 PDF 的左侧|漏洞|
|DIAGRAMNET-51874|VSDX 到 PDF - 输出中缺少内容和行|漏洞|
|DIAGRAMNET-51876|VSDX 到 PNG - 输出中的某些形状不正确|漏洞|
|DIAGRAMNET-51879|Visio 到 PDF - 输出不正确|漏洞|
|DIAGRAMNET-51894|加载 diagram 时出现 System.NullReferenceException|漏洞|
|DIAGRAMNET-51895|无法检索组属性数据，如 SelectionModel、DisplayMode|漏洞|

## **公共 API 和向后不兼容的更改**  ##
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。

#### 在页面中添加方法 AddShape ####
```
Diagram diagram = new Diagram();

// Get page object by index
Aspose.Diagram.Page page0 = diagram.Pages[0];
// set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import ole as Visio shape word
page0.AddShape(pinX, pinY, width, hieght, new FileStream( "imageword.emf", FileMode.OpenOrCreate), new FileStream( "wordsource.doc", FileMode.OpenOrCreate));
```
