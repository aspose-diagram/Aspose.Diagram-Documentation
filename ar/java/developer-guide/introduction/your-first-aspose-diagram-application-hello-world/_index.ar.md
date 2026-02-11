---
title: أول طلب Aspose.Diagram - Hello World
type: docs
weight: 30
url: /ar/java/your-first-aspose-diagram-application-hello-world/
description: توضح هذه الصفحة كيفية إنشاء التطبيق الأول باستخدام مكتبة Aspose.Diagram.
---
{{% alert color="primary" %}}

يوضح هذا البرنامج التعليمي كيفية إنشاء أول تطبيق (Hello World) باستخدام Aspose.Diagram "API البسيط. يقوم هذا التطبيق البسيط بإنشاء ملف Microsoft Visio بالنص" Hello World "في صفحة محددة.

{{% /alert %}}

## **إنشاء تطبيق Hello World**

تؤدي الخطوات أدناه إلى إنشاء تطبيق Hello World باستخدام Aspose.Diagram API:

1.  قم بإنشاء مثيل لـ[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) صف دراسي.
1.  إذا كان لديك ترخيص ، إذن[قم بتطبيقه](https://reference.aspose.com/diagram/java/com.aspose.diagram/License).
 إذا كنت تستخدم الإصدار التقييمي ، فتخط سطور التعليمات البرمجية المتعلقة بالترخيص.
1. قم بتكوين ملف Visio جديد ، أو افتح ملف Visio موجود.
1. قم بإنشاء مربع نص جديد.
1.  أدخل الكلمات**Hello World!** في مربع نص.
1. قم بإنشاء ملف Microsoft Visio المعدل.

يتم توضيح تنفيذ الخطوات المذكورة أعلاه في الأمثلة أدناه.

### **نموذج التعليمات البرمجية: إنشاء Diagram جديد**

المثال التالي ينشئ diagram جديد من الصفر ، يكتب Hello World! في الصفحة الأولى ويحفظ الملف Visio.

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

### **نموذج التعليمات البرمجية: فتح ملف موجود**

يفتح المثال التالي ملف قالب Microsoft Visio موجود باسم "Sample.vsdx" ، بإدخال "Hello World!" نص في الصفحة الأولى ويحفظ diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadVisioDiagram.class);   
// Open the stream. Read only access is enough for Aspose.Diagram to load a diagram.
InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

//Call the diagram constructor to load diagram from a VSDX stream
Diagram vsdDiagram = new Diagram(stream);
stream.close();

//Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load diagram from a VSS file
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
