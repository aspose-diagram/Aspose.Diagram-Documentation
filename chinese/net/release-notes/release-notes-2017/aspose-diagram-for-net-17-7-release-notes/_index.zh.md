---
title: Aspose.Diagram for .NET 17.7 发行说明
type: docs
weight: 60
url: /zh/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51204|diagram 保存后打印机纸张尺寸发生变化。|强化|
|DIAGRAMNET-51230|页边距值不正确。|强化|
|DIAGRAMNET-51274|添加对在形状级别插入注释的支持。|强化|
|DIAGRAMNET-51297|输入 VDX - SolutionXML 读取不正确。|强化|
|DIAGRAMNET-51061|将 VST 转换为 PNG 时缺少形状。|漏洞|
|DIAGRAMNET-51262|将 VSDM 转换为 SVG 时置换文本项。|漏洞|
|DIAGRAMNET-51276|VSD 到 SVG - 所有图标都无法正常显示。|漏洞|
|DIAGRAMNET-51277|VSDM 到 SVG - 缺少形状的阴影。|漏洞|
|DIAGRAMNET-51279|将 VSD 转换为 PDF 时缺少字符。|漏洞|
|DIAGRAMNET-51282|某些 vdx 文件在保存后损坏。|漏洞|
|DIAGRAMNET-51284-|DiagramException 在 vsdx 文件加载时发生。|漏洞|
|DIAGRAMNET-51285|VSD 到 PNG - 所有文本项都丢失了。|漏洞|
|DIAGRAMNET-51286|VSD 到 PNG - 形状的部分渲染。|漏洞|
|DIAGRAMNET-51288|将 VSDX 转换为 PNG 时出现无效颜色值错误。|漏洞|
|DIAGRAMNET-51289|页面级评论图标不显示文本。|漏洞|
|DIAGRAMNET-51290|Aspose.Diagram SetWidth 方法中的错误。|漏洞|
|DIAGRAMNET-51291|输出 VSDX - 直线设置连接线时布局不正确。|漏洞|
|DIAGRAMNET-51292|输出 VSDX - 连接线的文本项放错了位置。|漏洞|
|DIAGRAMNET-51293|VSDX 到 SVG - 一个附加标记与形状一起出现。|漏洞|
|DIAGRAMNET-51294|VSDM 到 SVG - 一个附加标记与形状一起出现。|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Page 类中添加 AddComment 方法**
Page 类公开的重载 AddComment 方法采用 Shape 类实例和评论的文本字符串。

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [在 Visio 绘图中添加形状级注释](/diagram/zh/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
