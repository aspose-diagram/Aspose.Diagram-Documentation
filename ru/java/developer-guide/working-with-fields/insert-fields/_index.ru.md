---
title: Создать, Вставить поля
type: docs
weight: 10
url: /ru/java/create-insert-fields/
description: Как создавать, вставлять поля с помощью Java Diagram API.
---
## **Вставить поле**
 Aspose.Diagram for Java позволяет создавать и вставлять[поле](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) на Microsoft Visio диаграммы из ваших собственных приложений, без автоматизации Microsoft Office.
### **Образец программирования**
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

