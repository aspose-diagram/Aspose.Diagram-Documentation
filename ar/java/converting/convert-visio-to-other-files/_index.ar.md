---
title:  قم بتحويل Visio إلى تنسيقات أخرى
linktitle:  قم بتحويل Visio إلى تنسيقات أخرى
type: docs
weight: 40
url: /ar/java/convert-visio-to-other-files/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى SVG،XPS ، XML ، XAML تنسيقات. تحويل VSD، VSS، VDW، VST، VSDX، VSSX، VSTX، VSDM، VSTM،VSSM إلى SVG،XPS، XML، XAML مع بضعة أسطر من التعليمات البرمجية.
---
## **التصدير إلى XML**
 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XML باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

- يعرف VDX XML diagram.
- يقوم VTX بتعريف قالب XML.
- يعرف VSX استنسل XML.

 ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) قرأ مُنشئو الفئة diagram ويتم استخدام طريقة الحفظ لحفظ أو تصدير diagram بتنسيق ملف مختلف. توضح مقتطفات التعليمات البرمجية في هذه المقالة كيفية استخدام طريقة Save لحفظ ملف Visio في[VDX](/diagram/ar/java/how-to-convert-a-visio-diagram/), [VTX](/diagram/ar/java/how-to-convert-a-visio-diagram/) و[VSX](/diagram/ar/java/how-to-convert-a-visio-diagram/).

توضح الصورة أدناه diagram الذي تم تصديره في قصاصات التعليمات البرمجية أدناه. يظهر الملف الذي تم تصديره قبل كل مقتطف رمز.

**A Microsoft Visio diagram على وشك التصدير.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/XWajazh.png)
### **تصدير VSD الى VDX**
VDX هو تنسيق ملف XML مستند إلى مخطط يسمح لك بحفظ الرسوم التخطيطية بتنسيق يمكن أن تقرأه منتجات بخلاف Microsoft Visio. إنه تنسيق مفيد لنقل المخططات بين تطبيقات البرامج والاحتفاظ بالبيانات القابلة للتحرير.

لتصدير VSD diagram إلى VDX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VDX.

**الملف VDX الذي تم تصديره.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/OJ1jpgh.png)
### **تصدير من VSD الى VSX**
VSX هو نسق XML لتعريف الإستنسل ، الكائنات الأساسية التي تم بناء diagram منها. عند تحويل ملف Visio إلى VSX ، يتم تصدير قوالب الإستنسل فقط.

لتصدير VSD diagram إلى VSX:

- قم بتكوين نسخة من الفئة Diagram.
- قم باستدعاء الأسلوب Save للفئة Diagram لكتابة ملف الرسم Visio إلى VSX.

توضح الصورة أدناه ملف الإخراج VSX. لاحظ أن الإستنسل المستخدم في diagram ، وليس diagram نفسه ، يتم تصديره.

**الملف VSX الذي تم تصديره.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/gkZrxCN.png)
### **تصدير VSD إلى VTX**
TVX هو تمثيل XML لملف قالب ويخزن إعدادات المستند.

لتصدير VSD diagram إلى VTX:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الأسلوب Save للفئة diagram لكتابة ملف الرسم Visio بتنسيق VTX.

توضح الصورة أدناه ملف الإخراج VTX.

**ملف الإخراج VTX.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/E6pUvGD.jpg)
### **التصدير إلى نموذج برمجة XML**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXML.class);

/* 1. Exporting VSDX to VDX */
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

//Save input VSD as VDX
diagram.save(dataDir + "ExportToXML_Out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
        
//Save input VSD as VSX
diagram.save(dataDir + "ExportToXML_Out.vsx", SaveFileFormat.VSX);
        
/* 3. Export VSD to VTX */
//Save input VSD as VTX
diagram.save(dataDir + "ExportToXML_Out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}
```
## **تصدير الى XPS**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى XPS باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.
 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

تأخذ مقتطفات التعليمات البرمجية في هذه المقالة diagram أدناه كمدخل. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.

**وثيقة المصدر.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/P3gaA34.png)

لتصدير VSD diagram إلى XPS:

1. قم بتكوين نسخة من الفئة Diagram.
1. اتصل بـ Diagram class 'Save method وقم بتعيين XPS كتنسيق الإخراج.

توضح الصورة أدناه ملف الإخراج XPS.

**الإخراج XPS.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/1ESRxSy.png)
### **التصدير إلى عينة برمجة XPS**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXPS.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir+ "ExportToXPS.vsd");

// Save as XPS
diagram.save(dataDir + "ExportToXPS_Out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```
## **تصدير Diagram إلى SVG**
 تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى SVG (Scalable Vector Graphics) باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى SVG ، قم بتنفيذ الخطوات التالية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين SVG كتنسيق التصدير.
### **تصدير عينة برمجية من Diagram إلى SVG**
توضح عينات الكود كيفية تصدير diagram إلى SVG باستخدام Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToSVG.class);

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save as SVG
diagram.save(dataDir+ "ExportToSVG_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **تصدير Diagram إلى XAML**
تشرح هذه المقالة كيفية تصدير Microsoft Visio diagram إلى XAML (لغة ترميز التطبيق الموسعة) باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) مُنشئ class لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير VSD diagram إلى XAML:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم باستدعاء الفئة "Save method" وقم بتعيين XAML كتنسيق التصدير.
### **التصدير إلى عينة برمجة XAML**
يوضح نموذج الكود كيفية تصدير diagram إلى XAML باستخدام Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToXAML.class); 

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");

// save as XAML
diagram.save(dataDir + "ExportToXAML_Out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```

## **تحويل Visio الرسم بأشكال انتقائية**
باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد مجموعة من الأشكال لتحويل رسم Visio إلى أي تنسيق مدعوم آخر. تقدم فئة RenderingSaveOptions عضو الأشكال للحفاظ على مجموعة الأشكال. كل فئة خيار حفظ هي الشكل الممتد لفئة RenderingSaveOptions.

لتصدير رسم Visio بأشكال انتقائية:

1. قم بتكوين نسخة من الفئة Diagram.
1. قم بإنشاء مثيل لأي فئة SaveOption لتحديد الإعدادات كما تم سردها هنا:[حدد Visio خيارات الحفظ](https://docs.aspose.com/diagram/java/save-a-visio-drawing-to-pdf-html-and-other-formats/#specifying-visio-save-options)
1. استدعاء طريقة حفظ لكائن الفئة Diagram وتمرير كائن فئة خيار الحفظ كمعامل.
### **تحويل Visio الرسم باستخدام عينة برمجة لأشكال انتقائية**
يوضح نموذج التعليمات البرمجية كيفية تصدير رسم بأشكال انتقائية Visio.

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";
		
// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.getPages().get(0).getShapes().getShape(1));
shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing
diagram.save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
```