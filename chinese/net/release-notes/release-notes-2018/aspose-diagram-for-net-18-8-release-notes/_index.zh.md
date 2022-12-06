---
title: Aspose.Diagram for .NET 18.8 发行说明
type: docs
weight: 50
url: /zh/net/aspose-diagram-for-net-18-8-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 18.8](https://www.nuget.org/packages/Aspose.Diagram/18.8.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-51500|图像渲染问题|强化|
|DIAGRAMNET-51504|添加对创建新审阅者的支持|强化|
|DIAGRAMNET-50953|将 VSDX 转换为 PNG 时，文本项会发生位移|漏洞|
|DIAGRAMNET-51122|将 VSD 转换为 PDF 时文本项的位置不正确|漏洞|
|DIAGRAMNET-51123|将 VSD 转换为 PDF 时，形状的文本被置换|漏洞|
|DIAGRAMNET-51408|VSD to Image - 字符与线重叠|漏洞|
|DIAGRAMNET-51499|Diagram.Save 方法抛出 OutOfMemoryException|漏洞|
|DIAGRAMNET-51501|形状在 VDX 文件中重叠|漏洞|
|DIAGRAMNET-51505|生成的 PDF 中缺少点|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
#### **添加审稿人**
{{< highlight "java" >}}

             Reviewer viewer = new Reviewer();

            viewer.Name.Value = "test";

            viewer.ReviewerID.Value = 3;

{{< /highlight >}}




