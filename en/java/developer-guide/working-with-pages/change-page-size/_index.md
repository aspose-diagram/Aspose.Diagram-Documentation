---
title: Change Page Size
type: docs
weight: 10
url: /java/change-page-size/
description: This section explains how to change page's size in a visio file with Aspose.Diagram.
---

## **Change Page Size**

The [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 
The [PageProps](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageProps) object represents the page attributes, such as the page width, height, and scale. This property can be used to change page size.

Use the PageProps property to change page size .
### **Set Page Size Programming Sample**
The following piece of code change page size from a diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeVisioPageSize.class);
      
// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// Set Page Size
page.getPageSheet().getPageProps().getPageHeight().setValue(8);
page.getPageSheet().getPageProps().getPageWidth().setValue(11);

// Save Visio
diagram.save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
