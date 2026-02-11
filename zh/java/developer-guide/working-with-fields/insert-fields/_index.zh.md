---
title: 创建、插入字段
type: docs
weight: 10
url: /zh/java/create-insert-fields/
description: 如何使用 Java Diagram API 创建、插入字段。
---
## **插入字段**
Aspose.Diagram for Java 让你创建和插入[场地](https://reference.aspose.com/diagram/java/com.aspose.diagram/field)从您自己的应用程序到 Microsoft Visio 图表，没有 Microsoft Office 自动化。
### **编程范例**
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

