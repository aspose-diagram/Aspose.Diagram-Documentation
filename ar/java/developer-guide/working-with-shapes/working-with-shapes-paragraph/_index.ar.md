---
title: العمل مع فقرة الأشكال
type: docs
weight: 40
url: /ar/java/working-with-shapes-paragraph/
---
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. تعيين فقرة الشكل.
#### **تعيين نموذج لبرمجة فقرة الشكل**
استخدم الكود التالي في تطبيق Java لضبط فقرة الشكل باستخدام Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```