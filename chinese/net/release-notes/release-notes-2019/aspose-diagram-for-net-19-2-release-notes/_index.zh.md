---
title: Aspose.Diagram for .NET 19.2 发行说明
type: docs
weight: 110
url: /zh/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50009|以 PDF 文件格式导出 VSD 绘图时心形混淆|强化|
|DIAGRAMNET-50010|VSD 到 PDF 导出具有并发点的多条锯齿线而不是单条曲线|强化|
|DIAGRAMNET-51257|导出图纸时添加对 NUBRS 线的支持|强化|
|DIAGRAMNET-51611|无法正确获取 Prop.Prompt.Value|强化|
|DIAGRAMNET-50355|曲线导出为直线|漏洞|
|DIAGRAMNET-50702|VSDX 到 PDF 导出 - 弯曲的连接器变成直的|漏洞|
|DIAGRAMNET-51348|VSDX 到 PDF - 字母呈现不正确|漏洞|
|DIAGRAMNET-51399|VSD 到 PNG - 曲线转换为直线|漏洞|
|DIAGRAMNET-51448|VSD 到 PNG - 网络一词周围缺少椭圆|漏洞|
|DIAGRAMNET-51472|VSD 到 PDF - 曲线导出为直线|漏洞|
|DIAGRAMNET-51507|VSDX 到 PNG - 输出中缺少填充的椭圆形|漏洞|
|DIAGRAMNET-51508|VSDX 到 SVG - 输出中缺少填充的椭圆形|漏洞|
|DIAGRAMNET-51537|VSDX 到 SVG - 当 VSDX 呈现为 PDF 时，弯曲连接器变为直连接器|漏洞|
|DIAGRAMNET-51540|转换后形状边缘变为正方形|漏洞|
|DIAGRAMNET-51577|VISIO 到 SVG - 输出不正确|漏洞|
|DIAGRAMNET-51592|转换时曲线变为直线|漏洞|
|DIAGRAMNET-51600|将 diagram 另存为另一种格式时，直线会变成尖峰|漏洞|
|DIAGRAMNET-51604|VSDX 到 PDF 转换错误 - 黑色省略号|漏洞|
|DIAGRAMNET-51605|更新 API 参考并添加有关 Shape.SetAngle() 方法的详细信息|漏洞|
|DIAGRAMNET-51610|VSDX 到 SVG - 文本未以正确的字体呈现|漏洞|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **在 Shape 中添加 InheritProps**
包含由主形状继承的形状的道具。

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
