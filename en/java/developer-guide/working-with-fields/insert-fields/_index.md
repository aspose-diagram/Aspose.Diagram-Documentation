---
title: Create, Insert fields
type: docs
weight: 10
url: /java/create-insert-fields/
description: How to create, insert fields using Java Diagram API .
---

## **Insert field**
Aspose.Diagram for Java lets you create and insert [field](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) to Microsoft Visio diagrams from within your own applications, without Microsoft Office Automation. 
### **Programming Sample**

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


