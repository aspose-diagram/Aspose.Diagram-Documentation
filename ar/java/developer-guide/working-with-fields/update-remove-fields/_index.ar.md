---
title: تحديث وإزالة الحقول
type: docs
weight: 20
url: /ar/java/update-remove-fields/
description: يشرح هذا القسم كيفية تحديث الحقول أو إزالتها.
---
## **تحديث الميدان**
 يتيح لك Aspose.Diagram for .NET التحديث والإزالة[مجال](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) إلى Microsoft Visio الرسوم البيانية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office.

 ال[مجال](https://reference.aspose.com/diagram/java/com.aspose.diagram/field) يمثل الكائن حقل نص في ملف[نص](https://reference.aspose.com/diagram/java/com.aspose.diagram/text) يجري. خاصية الحقل ، المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) فئة تدعم مجموعة من Aspose.Diagram.Field كائنات.
### **عينة البرمجة**
الجزء التالي من حقل تحديث التعليمات البرمجية في الشكل.

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


### **إزالة الحقل**
الجزء التالي من التعليمات البرمجية يزيل الحقل في الشكل.

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


