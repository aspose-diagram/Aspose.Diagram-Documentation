---
title: Aspose.Diagram for .NET 18.1 发行说明
type: docs
weight: 120
url: /zh/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50494|添加对复制/克隆 diagram 页面的支持|强化|
|DIAGRAMNET-51057|从 VSDM 中删除页面后命令按钮丢失|强化|
|DIAGRAMNET-51422|VSDX 到 PDF - 过程形状上的阴影被忽略|强化|
|DIAGRAMNET-50467|VSD 转PDF，公司企业logo错位|漏洞|
|DIAGRAMNET-50469|VSD 转PDF，radio shape text 比平时稍微up|漏洞|
|DIAGRAMNET-51199|将 VSDM 保存为 SVG 时标题文本未对齐|漏洞|
|DIAGRAMNET-51388|vsdx 文件加载和保存的问题|漏洞|
|DIAGRAMNET-51398|VSD 到 PNG - 文本位置不正确|漏洞|
|DIAGRAMNET-51407|VSD 到 JPEG - 文本项错位|漏洞|
|DIAGRAMNET-51419|vsdx 文件中的形状未正确调整大小|漏洞|
|DIAGRAMNET-51420|VSDX 加载和保存后文件损坏|漏洞|
|DIAGRAMNET-51421|VSDX 到 PDF - 文本的字体颜色不正确|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Page 类中添加 Copy 成员**
Copy 成员采用目标页面实例作为参数来克隆此页面。

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [将 Visio Page 复制到另一个 Page 实例](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
