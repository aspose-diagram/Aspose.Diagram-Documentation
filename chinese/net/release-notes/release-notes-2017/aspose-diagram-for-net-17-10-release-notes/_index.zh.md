---
title: Aspose.Diagram for .NET 17.10 发行说明
type: docs
weight: 30
url: /zh/net/aspose-diagram-for-net-17-10-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 17.10](https://www.nuget.org/packages/Aspose.Diagram/17.10.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51349|添加支持将绘图转换为与 PDF 相同区域的图像|强化|
|DIAGRAMNET-51352|访问嵌入式文件|强化|
|DIAGRAMNET-51085|在 VSDX 中保存时，公式在 Shapesheet 的控制选项卡下丢失|漏洞|
|DIAGRAMNET-51094|在放置梯形形状时保留控制选项卡下的默认设置|漏洞|
|DIAGRAMNET-51355|VSDX 到 PDF - 文本项目错放|漏洞|
|DIAGRAMNET-51356|VSDX 到 HTML - 文本项错位|漏洞|
|DIAGRAMNET-51357|VSDX的打开和保存例程-缺少注释的日期和编辑日期属性|漏洞|
|` `DIAGRAMNET-51358|加载 VSDX 绘图时出现空指针错误|漏洞|
|DIAGRAMNET-51359|加载后元素作者列表出错 VSDX|漏洞|
|DIAGRAMNET-51361|VSDX 到 VDX - 形状的不正确文本字体|漏洞|
|DIAGRAMNET-51363|VSDX的打开保存例程-Tabs部分变成自闭标签|漏洞|
|DIAGRAMNET-51365|VSD 到 PNG - 形状布局不正确|漏洞|
|DIAGRAMNET-51367|VSD 绘图导入 - 元素大师中的错误|漏洞|
|DIAGRAMNET-51368|VSD 到 PNG - 发生溢出错误|漏洞|
|DIAGRAMNET-51369|VSD 到 PDF - 底部的文本项目错位|漏洞|
|DIAGRAMNET-51371|VSDX 至 VSDX - 添加了其他文本项|漏洞|
|DIAGRAMNET-51373|VSDX 绘图的打开和保存例程缺少亚洲文字字体|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 ImageSaveOptions 中添加 SameAsPdfConversionArea**
指定是否像PDF一样保存区域。

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

Aspose.Diagram.Saving.ImageSaveOptions opts = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

opts.SameAsPdfConversionArea = true;

{{< /highlight >}}
