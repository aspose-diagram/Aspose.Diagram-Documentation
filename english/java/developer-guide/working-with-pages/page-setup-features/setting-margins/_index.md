---
title: Setting Margins
type: docs
weight: 20
url: /java/setting-margins/
description: This section explains how to set visio's page options with Aspose.Diagram.
---

{{% alert color="primary" %}}

Aspose.Diagram fully supports Microsoft Visio's page setup options. Developers may need to configure page setup settings for pages to control the printing process. This topic discusses how to use Aspose.Diagram to configure page margins.

{{% /alert %}}

## **Setting Margins**

Aspose.Diagram provides a class, [**Page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class contains a [**Pages**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) class.

The [**PageSheet**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) class provides the [**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) property is an object of the [**PageSheet**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **Page Margins**

Set page margins (PageTopMargin, PageBottomMargin, PageLeftMargin, PageRightMargin) using [**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) class members. A few of the methods are listed below which are used to specify page margins:

- [**PageTopMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)


{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageMargin-SetPageMargin.java" >}}