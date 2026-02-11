---
title: إنشاء وإدراج الحقول
type: docs
weight: 10
url: /ar/java/create-insert-fields/
description: كيفية إنشاء وإدخال الحقول باستخدام Java Diagram API.
---
## **أدخل الحقل**
 يتيح لك Aspose.Diagram for Java الإنشاء والإدراج[مجال](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) إلى Microsoft Visio الرسوم البيانية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.
### **عينة البرمجة**
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

