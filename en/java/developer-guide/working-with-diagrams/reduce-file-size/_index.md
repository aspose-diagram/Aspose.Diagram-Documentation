---
title: Reduce File Size
type: docs
weight: 50
url: /java/reduce-file-size/
description: This section explains how to reduce file size from a diagram with Aspose.Diagram.
---

## **Reduce File Size**
Aspose.Diagram for Java API allows developers to remove hidden info from a diagram to reduce file size. 
The [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) object represents the drawing area of a foreground page or a background page.In order to reduce file size, you can use [RemoveHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) properties in  **RemoveHiddenInformation()** method of [Diagram](https://reference.aspose.com/diagram/java) class. The code example below shows how to remove hidden info from diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}
```
