---
title: Update,Remove Fields
type: docs
weight: 20
url: /java/update-remove-fields/
description: This section explains how to update or remve fields.
---

## **Update Field**
Aspose.Diagram for .NET lets you update and remove [field](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 

The [Field](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) object represents text field in a [text](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) run. The field property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class supports a collection of Aspose.Diagram.Field objects.
### **Programming Sample**
The following piece of code update field in shape.

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Remove Field**
The following piece of code remove field in shape.

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


