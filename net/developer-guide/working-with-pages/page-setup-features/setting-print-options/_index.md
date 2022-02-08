---
title: Setting Print Options
type: docs
weight: 10
url: /net/setting-print-options/
description: This section explains how to set print options  with Aspose.Diagram.
---

{{% alert color="primary" %}}

Sometimes, it is necessary to configure page setup settings for pages to control printing. These page setup settings offer various options.

{{% /alert %}}

## **Setting Print Options**

Page setup options are fully supported in Aspose.Diagram. This article explains how to set page options with Aspose.Diagram and shows code samples for setting:

Aspose.Diagram provides a class, [**Page**](https://apireference.aspose.com/diagram/net/aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://apireference.aspose.com/diagram/net/aspose.diagram/page) class contains a [**Pages**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://apireference.aspose.com/diagram/net/aspose.diagram/page) class.

The [**PageSheet**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet) class provides the [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property is an object of the [**PageSheet**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **Print Page Orientation**

Print Page orientation can be set to portrait or landscape using the [**PrintProps**](https://apireference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) class' [**PrintPageOrientation**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) property. The [**PrintPageOrientation**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) property accepts one of the pre-defined values in the [**PrintPageOrientationValue**](https://apireference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue) enumeration, listed below.

|**Print Page Orientation Types**|**Description**|
| :- | :- |
|SameAsPrinter|Same As Printer orientation|
|Landscape|Landscape orientation|
|Portrait|Portrait orientation|

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageOrientation.cs" >}}

### **Scaling Factor**

It is possible to reduce or enlarge a page's size by adjusting the scaling factor with the [**ScaleX**](https://apireference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex) property.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageOrientation-SetPageScale.cs" >}}
