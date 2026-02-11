---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/java/convert-visio-to-image/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات صور مختلفة. تحويل Visio،VSD ، VSS ، VDW ، VST ، VSDX ، VSSX ، VSTX ، VSDM ، VSTM،VSSM إلى PNG ، JPEG ، BMP من الصور.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 استخدم ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class 'المُنشئ لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم. تُظهر الصورة أدناه ملف VSD على وشك أن يتم حفظه بتنسيق PNG. يمكنك استخدام تنسيقات diagram أخرى (VSS ، VSSX ، VSSM ، VDX ، VST ، VSTX ، VSTM ، VDX ، VTX أو VSX) أيضًا.
**الملف المصدر. لاحظ أن تسميات السهم والمثلث بخط غامق.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/WOV36ek.png)

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.

**ملف الإخراج PNG.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/WOV36ek.png)
### **التصدير إلى نموذج برمجة ملفات الصور**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportToImage.class);

// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save as PNG
diagram.save(dataDir+ "ExportToImage_Out.png", SaveFileFormat.PNG);

{{< /highlight >}}
```

من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExportPageToImage.class);     
// load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

//Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.setPageIndex(0);

//Save resultant Image file
diagram.save(dataDir + "ExportPageToImage_Out.png", options);

{{< /highlight >}}
```