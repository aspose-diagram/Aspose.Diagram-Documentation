---
title: Aspose.Diagram for .NET 17.02.0 发行说明
type: docs
weight: 110
url: /zh/net/aspose-diagram-for-net-17-02-0-release-notes/
---
{{% alert color="primary" %}} 

此页面包含发行说明[Aspose.Diagram for .NET 17.02.0](https://www.nuget.org/packages/Aspose.Diagram/17.2.0).

{{% /alert %}} 
## **改进和变化**

|**钥匙**|**概括**|**类别**|
|:- |:- |:- |
|DIAGRAMNET-50018|添加了对 CLS 兼容的支持。|新功能|
|DIAGRAMNET-51110|与仪表集成。|新功能|
|DIAGRAMNET-51143|能够获得给定形状的组。|新功能|
|DIAGRAMNET-51144|能够获得给定形状的父级。|新功能|
|DIAGRAMNET-50149|VSD 到 PDF 转换，组形状的背景颜色阴影正在改变。|漏洞|
|DIAGRAMNET-50579|VSDX 到 PDF 转换，形状的背景颜色不正确。|漏洞|
|DIAGRAMNET-50984|将 VSDX 转换为 PNG 时，表格的边框线丢失。|漏洞|
|DIAGRAMNET-50985|将 VSDX 转换为 PNG 时，文本项未正确对齐。|漏洞|
|DIAGRAMNET-50999|在将 VSD 转换为 PNG 时呈现不正确的形状颜色。|漏洞|
|DIAGRAMNET-51002|HTMLSaveOptions.DefaultFont 属性未按预期工作。|漏洞|
|DIAGRAMNET-51049|将 VSD 转换为 HTML 时，形状颜色未正确呈现。|漏洞|
|DIAGRAMNET-51080|在 EMF 中保存时形状的文本对齐错误。|漏洞|
|DIAGRAMNET-51132|将 VSD 转换为 PDF 时，圆角会发生变化。|漏洞|
|DIAGRAMNET-51133|将 VSD 转换为 PDF 时，动态箭头连接器的布局发生了变化。|漏洞|
|DIAGRAMNET-51135|Visio 形状在将 VSDX 转换为 PDF 时发生位移。|漏洞|
|DIAGRAMNET-51136|在将 VSDX 转换为 PDF 时，垂直文本显示为水平文本。|漏洞|
|DIAGRAMNET-51140|将 VSDX 转换为 PDF 时，垂直文本框悬垂在节点的边缘。|漏洞|
|DIAGRAMNET-51138|VSDX diagram 载入错误。|例外|
|DIAGRAMNET-51139|将 VSDX 转换为 HTML 时发生无法访问文件错误。|例外|
|DIAGRAMNET-51148|Diagram 处的 NullReferenceException。将 VSD 转换为 HTML 时保存。|例外|
|DIAGRAMNET-51149|NullReferenceException at Diagram.Save when CustomProp.Name property is not set|例外|
## **公共 API 和向后不兼容的更改**
以下是对公众 API 所做的任何更改的列表，例如添加、重命名、删除或弃用成员，以及对 Aspose.Diagram for .NET 所做的任何非向后兼容更改。如果您对列出的任何更改有疑虑，请在这[Aspose.Diagram 支持论坛](https://forum.aspose.com/c/diagram/17).
### **添加 Shape.ParentShape 属性**
Shape.ParentShape 属性允许获取最近形状的父形状。

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram("Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Shape parentShape = shape.ParentShape;

Console.WriteLine("Parent Shape's Properties:");

Console.WriteLine("Shape ID: " + parentShape.ID);

Console.WriteLine("Shape Name: " + parentShape.Name);

Console.WriteLine("Shape Type: " + parentShape.Type);

{{< /highlight >}}
### **添加 Shape.IsInGroup 方法**
Shape.IsInGroup 方法允许检测最近的形状是否是任何组形状的一部分。

{{< highlight "java" >}}

 // Call a Diagram class constructor to load the VSD diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get a sub-shape by page name, group shape ID, and then sub-shape ID

Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);

Console.WriteLine("Is it in a Group: " + shape.IsInGroup());

{{< /highlight >}}
### **添加计量类**
添加了 Metered 类。它允许开发人员解锁 Aspose.Diagram API 的评估限制以及跟踪和维护 API 许可证。它还监视 Aspose.Diagram API 的常规使用情况。

{{< highlight "java" >}}

 // Initialize a Metered license class object

Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();

// apply public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

{{< /highlight >}}
### **使用示例**
请查看 Aspose.Diagram Wiki 文档中添加的帮助主题列表：

1. [设置公钥和私钥以应用计量许可证](/diagram/zh/net/licensing/#licensing-setpublicandprivatekeystoapplymeteredlicense)
1. [检索子形状的父形状](/diagram/zh/net/add-retrieve-copy-and-read-visio-shape-data/#add-retrieve-copyandreadvisioshapedata-retrievetheparentshapeofasub-shape)
1. [验证 Visio 形状是否在一组形状中](https://docs.aspose.com/diagram/net/group-convert-and-verify-shapes/)
