---
title: 使用超链接
type: docs
weight: 160
url: /zh/net/working-with-hyperlinks/
description: 本节介绍如何在带有 Aspose.Diagram 的 Visio 形状中添加或获取超链接。
---
## **将超链接添加到 Visio 形状**
Microsoft Office Visio 支持给任意形状添加超链接。超链接可以链接到当前绘图中的另一个页面或形状、另一个绘图中的页面或形状、Visio 绘图以外的文档、网站、FTP 站点或电子邮件地址。开发人员可以使用 Aspose.Diagram API 轻松地为 Visio 形状添加超链接。

在多页 Visio 绘图中，超链接可以将您从一种形状导航到许多其他类型的链接。[超链接集合](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection)暴露的[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类提供 Add 方法，可用于添加形状的超链接。

识别 Microsoft Office Visio 中的属性：

1. 在 Visio diagram 中，右键单击一个形状。
1. 选择**超链接。**
1. 设置现有属性
1. 按**好的**按钮

**形状的超链接数据，如 Microsoft Visio 所示**

![待办事项：图片_替代_文本](working-with-hyperlinks_1.png)
### **添加超链接编程示例**
下面的代码片段添加了形状的超链接数据。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **获取 Visio 形状的超链接数据**
开发人员可以使用与他们相同的方式从 Visio 形状中检索所有超链接[读取 Visio 形状数据](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/)使用[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

在多页 Visio 绘图中，超链接可以将您从一种形状导航到许多其他类型的链接。[超链接集合](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection)暴露的[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类允许开发人员检索超链接。

识别 Microsoft Office Visio 中的属性：

1. 在 diagram 中，右键单击一个形状。
1. 选择**超链接。**

对话框中列出了任何现有属性。
**形状的超链接数据，如 Microsoft Visio 所示**

![待办事项：图片_替代_文本](working-with-hyperlinks_1.png)

**显示形状数据输出的控制台窗口**

![待办事项：图片_替代_文本](working-with-hyperlinks_3.png)
### **获取超链接编程示例**
下面的代码片段读取形状的超链接数据。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}

