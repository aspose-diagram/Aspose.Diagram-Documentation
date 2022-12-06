---
title: Aspose.Diagram for .NET 22.6 发行说明
type: docs
weight: 22
url: /zh/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 22.6 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-52826|将 VSDM 保存为 PDF 时链接断开|强化|
|DIAGRAMNET-52851|某些形状在转换为 svg 后会失去曲线|强化|
|DIAGRAMNET-52858|HTML 中的图像质量|强化|
|DIAGRAMNET-52825|导出为 HTML 问题|漏洞|
|DIAGRAMNET-52832|Visio 到 PDF/SVG - 旋转的文本位置已更改|漏洞|
|DIAGRAMNET-52840|HTML 预览中的元素模糊|漏洞|
|DIAGRAMNET-52842|自动调整页面不自动调整|漏洞|
|DIAGRAMNET-52849|转换后光栅图像未按比例缩小|漏洞|
|DIAGRAMNET-52852|VSD 打开错误 - Aspose.Diagram.DiagramException|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。
### **在 HTMLSaveOptions 中添加分辨率**
- 获取或设置生成的 html 的分辨率，以每英寸点数为单位。

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
