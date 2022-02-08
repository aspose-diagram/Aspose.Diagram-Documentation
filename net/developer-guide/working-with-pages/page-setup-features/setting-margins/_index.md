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

Aspose.Diagram provides a class, [**Page**](https://apireference.aspose.com/diagram/net/aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://apireference.aspose.com/diagram/net/aspose.diagram/page) class contains a [**Pages**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://apireference.aspose.com/diagram/net/aspose.diagram/page) class.

The [**PageSheet**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet) class provides the [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property is an object of the [**PageSheet**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **Page Margins**

Set page margins (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) using [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) class members. A few of the methods are listed below which are used to specify page margins:

- [**PageTopMargin**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageMargin-SetPageMargin.cs" >}}