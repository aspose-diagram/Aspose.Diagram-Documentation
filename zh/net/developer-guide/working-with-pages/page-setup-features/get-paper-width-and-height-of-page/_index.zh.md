---
title: 获取页面的纸张宽度和高度
type: docs
weight: 50
url: /zh/net/get-paper-width-and-height-of-page/
description: 本节介绍如何使用 Aspose.Diagram 获取 visio 页面的纸张大小。
---
## **可能的使用场景**

有时，您需要知道纸张尺寸的宽度和高度，因为它已在页面的页面设置中设置。请使用[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)和[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)用于此目的的属性。

## **获取页面的页面宽度和页面高度 Prop of Page**

下面的示例代码解释了[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)和[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)特性。

### **示例代码**


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}

