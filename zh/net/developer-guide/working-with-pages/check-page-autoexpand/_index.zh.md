---
title: 检查页面自动扩展
type: docs
weight: 10
url: /zh/net/check-page-autoexpand/
description: 本节介绍如何检查或更改页面是否在带有 Aspose.Diagram 的 visio 文件中自动展开。
---
## **更改页面大小**

这[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)对象表示前景页面或背景页面的绘图区域。公开的 Pages 属性[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类支持 Aspose.Diagram.Page 对象的集合。
这[页面道具](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops)对象表示页面属性，例如页面宽度、高度和比例。此属性可用于检查页面的自动扩展。

使用 PageProps 属性检查页面的自动展开。
### **设置页面大小编程示例**
以下代码检查页面从 diagram 自动扩展。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
