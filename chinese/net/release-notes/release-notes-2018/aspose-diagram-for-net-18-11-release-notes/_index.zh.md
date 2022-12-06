---
title: Aspose.Diagram for .NET 18.11 发行说明
type: docs
weight: 20
url: /zh/net/aspose-diagram-for-net-18-11-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50410|MilestoneHelper - 添加对自定义日期字符串格式设置器的支持|强化|
|DIAGRAMNET-51568|在 SVG 的 SaveOptions 中添加设置 ViewBox 的选项|强化|
|DIAGRAMNET-51580|Aspose.Diagram 创建带有指南的 SVG 而 MS Visio 没有|强化|
|DIAGRAMNET-51556|Shape.ToImage 方法未生成正确的图像|漏洞|
|DIAGRAMNET-51557|Shape.ToImage 方法在复制页面的情况下返回空白图像|漏洞|
|DIAGRAMNET-51570|Shape.ToImage 方法未生成正确的图像|漏洞|
|DIAGRAMNET-51576|VSDX 到 PDF - 缺少文本块|漏洞|
|DIAGRAMNET-51578|VSDX 图像导致 StackOverFlowException|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 SVGSaveOptions 中添加 SVGFitToViewPort**
如果此属性为真，则生成的 SVG 将适合视口。

{{< highlight "java" >}}

 SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

{{< /highlight >}}
### **在 RenderingSaveOptions 中添加 ExportGuideShapes**
定义是否需要导出导向形状。

{{< highlight "java" >}}

 Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();

o.ExportGuideShapes = false;

{{< /highlight >}}
### **在 MilestoneHelper 中添加 DateFormatString**
DateFormat 形状字符串

{{< highlight "java" >}}

 milestoneHelper.DateFormatString = "yyyy/mm/dd";

{{< /highlight >}}
