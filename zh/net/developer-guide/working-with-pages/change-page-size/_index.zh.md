---
title: 更改页面大小
type: docs
weight: 10
url: /zh/net/change-page-size/
description: 本节介绍如何使用 Aspose.Diagram 更改 visio 文件中的页面大小。
---
## **更改页面大小**

这[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)对象表示前景页面或背景页面的绘图区域。公开的 Pages 属性[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类支持 Aspose.Diagram.Page 对象的集合。
这[页面道具](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops)对象表示页面属性，例如页面宽度、高度和比例。此属性可用于更改页面大小。

使用 PageProps 属性更改页面大小。
### **设置页面大小编程示例**
以下代码段从 diagram 更改页面大小。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

