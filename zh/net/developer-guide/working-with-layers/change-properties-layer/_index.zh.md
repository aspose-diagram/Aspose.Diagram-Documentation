---
title: 更改图层属性
type: docs
weight: 130
url: /zh/net/change-properties-layer/
description: 本节介绍如何使用 Aspose.Diagram 更改图层的属性。
---
## **在 Visio 中更改图层属性**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)允许在 Microsoft Office Visio diagram 中更改图层的属性。每个形状都可以属于多个图层，因此开发人员可以更改图层的属性以满足最终用户的需求。这[页表](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)类对象提供图层，允许在 Visio 绘图中添加和删除图层对象。用户可以管理[层](https://reference.aspose.com/diagram/net/aspose.diagram/layer)以编程方式使用 Aspose.Diagram API 的属性如下：
### **更改层属性编程示例**
以下代码有助于更改层的属性。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
