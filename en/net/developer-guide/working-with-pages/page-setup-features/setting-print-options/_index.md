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

Aspose.Diagram provides a class, [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class contains a [**Pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class.

The [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class provides the [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property is an object of the [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **Print Page Orientation**

Print Page orientation can be set to portrait or landscape using the [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) class' [**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) property. The [**PrintPageOrientation**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation) property accepts one of the pre-defined values in the [**PrintPageOrientationValue**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue) enumeration, listed below.

|**Print Page Orientation Types**|**Description**|
| :- | :- |
|SameAsPrinter|Same As Printer orientation|
|Landscape|Landscape orientation|
|Portrait|Portrait orientation|

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}
```

### **Scaling Factor**

It is possible to reduce or enlarge a page's size by adjusting the scaling factor with the [**ScaleX**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex) property.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}
```
