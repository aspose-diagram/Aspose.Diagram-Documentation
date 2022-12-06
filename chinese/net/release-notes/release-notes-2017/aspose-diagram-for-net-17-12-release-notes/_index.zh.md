---
title: Aspose.Diagram for .NET 17.12 发行说明
type: docs
weight: 10
url: /zh/net/aspose-diagram-for-net-17-12-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 17.12](https://www.nuget.org/packages/Aspose.Diagram/17.12.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50016|添加对复制/克隆形状的支持|强化|
|DIAGRAMNET-50677|提供单个 API 将 Visio 形状转换为 PDF|强化|
|DIAGRAMNET-50678|提供单个 API 将 Visio 形状转换为 HTML|强化|
|DIAGRAMNET-50762|The parsing error of the long attributes value occurred while generate a VDX diagram|漏洞|
|DIAGRAMNET-51401|输出 VSDX - Shapes 中的控件不起作用|漏洞|
|DIAGRAMNET-51402|VSDX to image - 不保留 OLE 对象|漏洞|
|DIAGRAMNET-51406|VSD 到图像 - 出现其他字符|漏洞|
|DIAGRAMNET-51410|VSD 到 PDF - 所有页面的页码保持为 4|漏洞|
|DIAGRAMNET-51411|VSD 到图像 - 页码在所有页面中保持为 4|漏洞|
|DIAGRAMNET-51414|VSDX 到 PDF - 缺少形状的内容|漏洞|
|DIAGRAMNET-51415|VSDX 到 PDF - 形状的背景颜色不正确|漏洞|
|DIAGRAMNET-51416|VSDX 到 HTML - 形状的背景颜色不正确|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Shape 类中添加 Copy 成员**
Copy 成员采用目标形状实例作为参数来克隆此形状。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
### **在 Shape 类中添加 ToPdf 成员**
ToPdf 成员将形状转换为 PDF 格式。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf("e:\\out.pdf");

{{< /highlight >}}
### **在 Shape 类中添加 ToHTML 成员**
ToHTML 成员将形状转换为 PDF 格式。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML("e:\\out.pdf", hs);

{{< /highlight >}}
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [将 Visio Shape 复制到另一个 Shape 实例](/diagram/zh/net/add-2c-retrieve-2c-copy-and-read-visio-shape-data-html/#add-retrieve-copyandreadvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [将 Visio 形状转换为 PDF](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-pdf/)
1. [将 Visio 形状转换为 HTML](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-html/)
