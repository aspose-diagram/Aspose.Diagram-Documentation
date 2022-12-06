---
title: Aspose.Diagram for .NET 22.5 发行说明
type: docs
weight: 23
url: /zh/net/aspose-diagram-for-net-22-5-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 22.5 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-52802|公式/值不刷新字段|强化|
|DIAGRAMNET-52803|VSDX 到 HTML：在程序完全执行之前，输出文件不保存在异步方法中|强化|
|DIAGRAMNET-52793|API 不适用于有效的许可证 22.4 版本|漏洞|
|DIAGRAMNET-52806|从 VSDX 转移 PDF 中的缩进|漏洞|
|DIAGRAMNET-52807|将 .vsdx 文件转换为 pdf 时，表格中的文本被删除 [续]|漏洞|
|DIAGRAMNET-52808|将 VSDX 转换为 PDF 时出现问题 [续]|漏洞|
|DIAGRAMNET-52810|Visio 保存为图像的形状是错误的|漏洞|
|DIAGRAMNET-52811|将 Visio 保存为 HTML 后形状丢失|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。
### **在字段中添加 DisplayValue**
- 获取该字段的格式化字符串值。

{{< highlight "java" >}}
String str = shape.Fields[0].DisplayValue;
{{< /highlight >}}

### **在 Shape 中添加 InheritParas**
- 包含由父样式和主样式继承的形状的参数

{{< highlight "java" >}}
ParaCollection paras = shape.InheritParas;
Console.WriteLine(paras[0].HorzAlign.Value);
{{< /highlight >}}