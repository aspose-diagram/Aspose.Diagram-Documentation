---
title: Public API Changes in Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /java/public-api-changes-in-aspose-diagram-6-7-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 6.6.0 to 6.7.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Adds detectFileFormat method in FileFormatUtil class**
It detects and returns the information about the format of a stored Visio diagram in an input stream. Please check this code example:

**Java**

{{< highlight java >}}

 String dataDir = "c:\\temp\\";

// Open the stream. Read only access to load a Visio diagram.

InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

// detect file format using an input stream

FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format

System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
