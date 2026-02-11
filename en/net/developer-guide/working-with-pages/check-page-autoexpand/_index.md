---
title: Check Page Autoexpand
type: docs
weight: 10
url: /net/check-page-autoexpand/
description: This section explains how to check or change page is auto expand in a visio file with Aspose.Diagram.
---

## **Change Page Size**

The [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 
The [PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) object represents the page attributes, such as the page width, height, and scale. This property can be used to check page's autoexpand.

Use the PageProps property to check page's autoexpand.
### **Set Page Size Programming Sample**
The following piece of code check page's autoexpand from a diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

