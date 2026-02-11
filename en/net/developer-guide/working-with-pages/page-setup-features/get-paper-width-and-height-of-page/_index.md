---
title: Get Paper Width and Height of Page
type: docs
weight: 50
url: /net/get-paper-width-and-height-of-page/
description: This section explains how to get paper size of the visio page with Aspose.Diagram.
---

## **Possible Usage Scenarios**

Sometimes, you need to know the width and height of paper size as it has been set in page setup of the page. Please use the [**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth) and [**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight) properties for this purpose.

## **Get Page Width and Height of Page Prop of Page**

The following sample code explains the usage of [**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth) and [**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight) properties.

### **Sample Code**


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

