---
title: Setting Margins
type: docs
weight: 20
url: /net/setting-margins/
description: This section explains how to set visio's page options with Aspose.Diagram.
---

{{% alert color="primary" %}}

Aspose.Diagram fully supports Microsoft Visio's page setup options. Developers may need to configure page setup settings for pages to control the printing process. This topic discusses how to use Aspose.Diagram to configure page margins.

{{% /alert %}}

## **Setting Margins**

Aspose.Diagram provides a class, [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class contains a [**Pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class.

The [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class provides the [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property is an object of the [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **Page Margins**

Set page margins (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) using [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) class members. A few of the methods are listed below which are used to specify page margins:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.Pages[0].PageSheet.PrintProps.PageLeftMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageRightMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageTopMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageBottomMargin.Value = 0.01;
{{< /highlight >}}
```