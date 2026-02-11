---
title: Setting FitToSheetAcross
type: docs
weight: 10
url: /net/setting-fittosheetacross/
description: This section explains how to set fittosheetacross  with Aspose.Diagram.
---

{{% alert color="primary" %}}

Sometimes, it is necessary to configure page setup settings for pages to control printing. These page setup settings offer various options.

{{% /alert %}}

## **Setting FitToSheetAcross**

Page setup options are fully supported in Aspose.Diagram. This article explains how to set page options with Aspose.Diagram and shows code samples for setting:

Aspose.Diagram provides a class, [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page), that represents a Microsoft Visio file. The [**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class contains a [**Pages**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) collection that allows access to each page in the Visio file. A page is represented by the [**Page**](https://reference.aspose.com/diagram/net/aspose.diagram/page) class.

The [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class provides the [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property that is used to set the page setup options of the page. In fact, this [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) property is an object of the [**PageSheet**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) class used to set different page layout options for a printed page. The [**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)  class provides various properties used to set page setup options. Some of these properties are discussed below.

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


