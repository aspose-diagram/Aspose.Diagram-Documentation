---
title: Aspose.Diagram for .NET 21.11 发行说明
type: docs
weight: 2
url: /zh/net/aspose-diagram-for-net-21-11-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 21.11 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51111|将 VDX 转换为 EMF 时，圆圈的渐变填充是错误的|强化|
|DIAGRAMNET-52377|添加旧版本 3 加载 vsd 的支持|强化|
|DIAGRAMNET-51364|VSDX 到 PNG - 缺少 OLE 嵌入对象的文本|漏洞|
|DIAGRAMNET-52329|VSDX 到 HTML - 输出中不存在表情符号|漏洞|
|DIAGRAMNET-52345|保存 Diagram 文件后页眉页脚丢失|漏洞|
|DIAGRAMNET-52349|Visio 到 HTML - 左右边缘被切割|漏洞|
|DIAGRAMNET-52374|保存为 PDF 时出现 ArgumentOutOfRangeException|漏洞|
|DIAGRAMNET-52386|为什么有些 diagram 页面可以复制而有些不能使用 Page.Copy()？|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。


### **在形状中添加预设主题**
- 将预设主题应用于此形状。

{{< highlight "java" >}}

shape.PresetTheme = PresetThemeValue.Bubble;

{{< /highlight >}}


### **在形状中添加 PresetThemeVariant**
- 将预设主题变体应用于此形状

{{< highlight "java" >}}

shape.PresetThemeVariant = PresetThemeVariantValue.Variant1;

{{< /highlight >}}

### **在形状中添加 PresetThemeQuickStyle**
- 将预设主题变体 quickstyle 应用于此形状

{{< highlight "java" >}}

 shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle1;

{{< /highlight >}}
