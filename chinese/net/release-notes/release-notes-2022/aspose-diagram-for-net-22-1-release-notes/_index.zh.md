---
title: Aspose.Diagram for .NET 22.1 发行说明
type: docs
weight: 27
url: /zh/net/aspose-diagram-for-net-22-1-release-notes/
---
{{% alert color="primary" %}} 

此页面包含 Aspose.Diagram for .NET 22.1 的发行说明信息。

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50560|支持将图表保存为带有或不带有嵌入式资源的 HTML|强化|
|DIAGRAMNET-52499|添加对将 html 保存到单个流的支持|强化|
|DIAGRAMNET-50562|VSDX 到 PDF - 输出中缺少形状|漏洞|
|DIAGRAMNET-50780|将 VSDX 保存为 PDF 时表格的边框线不可见|漏洞|
|DIAGRAMNET-50962|将 VSDX 转换为 PNG 时缺少表格的边框线|漏洞|
|DIAGRAMNET-50992|将 VSDX 转换为 PDF 时，表格的左边框线不可见|漏洞|
|DIAGRAMNET-51034|将 VSDX 转换为 PDF 时缺少形状的阴影|漏洞|
|DIAGRAMNET-51186|将 VSD 转换为 PDF 时元类型形状的布局不正确|漏洞|
|DIAGRAMNET-51226|Aspose.Diagram 17.3.0：保存到 HTML 流不嵌入外部资源|漏洞|
|DIAGRAMNET-52506|Page.Copy() 不会复制开发人员的更改|漏洞|

## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在Aspose.Diagram 支持论坛。


### **在 HTMLSaveOptions 中添加 SaveAsSingleFile**
- 指示是否将 html 保存为单个文件。

{{< highlight "java" >}}

    HTMLSaveOptions ho = new HTMLSaveOptions();
    ho.SaveAsSingleFile = true;

{{< /highlight >}}