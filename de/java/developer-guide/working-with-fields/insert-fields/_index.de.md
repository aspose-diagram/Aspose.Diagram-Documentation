---
title: Felder erstellen, einfügen
type: docs
weight: 10
url: /de/java/create-insert-fields/
description: So erstellen Sie Felder mit Java Diagram API .
---
## **Feld einfügen**
 Aspose.Diagram for Java lässt Sie erstellen und einfügen[aufstellen](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) bis Microsoft Visio Diagramme aus eigenen Applikationen, ohne Microsoft Office Automatisierung.
### **Programmierbeispiel**

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


