---
title: Change Page Size
type: docs
weight: 10
url: /net/change-page-size/
description: This section explains how to change page's size in a visio file with Aspose.Diagram.
---

## **Change Page Size**

The [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 
The [PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) object represents the page attributes, such as the page width, height, and scale. This property can be used to change page size.

Use the PageProps property to change page size .
### **Set Page Size Programming Sample**
The following piece of code change page size from a diagram.


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

