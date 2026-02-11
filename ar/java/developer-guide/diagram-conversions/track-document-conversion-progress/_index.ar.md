---
title: تتبع تقدم تحويل المستند
type: docs
weight: 970
url: /ar/java/track-document-conversion-progress/
description: يشرح هذا القسم كيفية تتبع تقدم التحويل لملفات visio باستخدام Aspose.Diagram.
---
## **سيناريوهات الاستخدام الممكنة**

في بعض الأحيان ، قد يستغرق تحويل ملفات visio الكبيرة بعض الوقت. خلال هذا الوقت ، قد ترغب في إظهار تقدم تحويل المستند بدلاً من مجرد شاشة تحميل لتحسين إمكانية استخدام التطبيق الخاص بك. يدعم Aspose.Diagram تتبع عملية تحويل المستندات من خلال توفير واجهة IPageSavingCallback. توفر واجهة IPageSavingCallback أساليب PageStartSaving و PageEndSaving التي يمكنك تنفيذها في الفصل الدراسي المخصص. يمكنك أيضًا التحكم في الصفحات التي يتم عرضها كما هو موضح في حرف T.*estDiagramPageSavingCallback*فئة مخصصة.

## **تتبع تقدم تحويل المستند**

 نموذج التعليمات البرمجية التالي بتحميل[المصدر visio ملف](Drawing1.vsdx) ويطبع تقدم التحويل في وحدة التحكم باستخدام ملف*TestPageSavingCallback*فئة مخصصة تقوم بتنفيذ واجهة IPageSavingCallback.

## **عينة من الرموز**

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

ما يلي هو رمز*TestDiagramPageSavingCallback*فئة مخصصة.

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

## **إخراج وحدة التحكم**

ابدأ بحفظ فهرس الصفحة 0 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 0 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 1 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 1 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 2 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 2 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 3 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 3 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 4 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 4 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 5 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 5 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 6 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 6 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 7 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 7 من الصفحات 11</br>
ابدأ بحفظ فهرس الصفحة 8 من الصفحات 11</br>
نهاية فهرس صفحة الحفظ 8 من الصفحات 11
