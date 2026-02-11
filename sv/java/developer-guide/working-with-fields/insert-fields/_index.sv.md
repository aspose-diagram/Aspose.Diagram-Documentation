---
title: Skapa, infoga fält
type: docs
weight: 10
url: /sv/java/create-insert-fields/
description: Så här skapar du, infoga fält med Java Diagram API .
---
## **Infoga fält**
 Aspose.Diagram for Java låter dig skapa och infoga[fält](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) till Microsoft Visio diagram från dina egna applikationer, utan Microsoft Office Automation.
### **Programmeringsexempel**
```
{{< highlight "java" >}}
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
```

