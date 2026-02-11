---
title: Check Page Autoexpand
type: docs
weight: 10
url: /java/check-page-autoexpand/
description: This section explains how to check or change page is auto expand in a visio file with Aspose.Diagram.
---

## **Check page AutoExpand**

The [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 
The [PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) object represents the page attributes, such as the page width, height, and scale. This property can be used to check page's autoexpand.

Use the PageProps property to check page's autoexpand.
### **Check Page AutoExpand Programming Sample**
The following piece of code check page's autoexpand from a diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CheckChangeAutoExpand.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Page-2");
// Get Page autoexpand
boolean isAutoExpand = page.getPageSheet().getPageProps().getDrawingResizeType().getValue() == DrawingResizeTypeValue.AUTOMATICALLY ? true : false;
//Set Page autoexpand
page.getPageSheet().getPageProps().getDrawingResizeType().setValue(DrawingResizeTypeValue.NOT_AUTOMATICALLY);

// Save Visio
diagram.save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

