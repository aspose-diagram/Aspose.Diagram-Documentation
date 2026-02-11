---
title:  تحويل Visio إلى تنسيقات الصور
linktitle: تحويل Visio إلى صور
type: docs
weight: 20
url: /ar/net/convert-visio-to-image/
description: يوضح لك هذا الموضوع كيفية السماح Aspose.Diagram بتحويل Visio إلى تنسيقات صور مختلفة. تحويل Visio،VSD ، VSS ، VDW ، VST ، VSDX ، VSSX ، VSTX ، VSDM ، VSTM،VSSM إلى PNG ، JPEG ، BMP من الصور.
---
## **تصدير المخططات إلى تنسيقات ملفات الصور**
 يشرح هذا المقال كيفية تصدير Microsoft Visio diagram إلى صورة باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API. استخدم[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) مُنشئ الفئة لقراءة ملفات diagram وطريقة Save لتصدير diagram إلى أي تنسيق صورة مدعوم.

لتصدير diagram إلى صورة:

- قم بتكوين نسخة من الفئة Diagram.
- اتصل بـ Diagram class 'Save method وقم بتعيين تنسيق الصورة الذي تريد التصدير إليه ، ملف صورة الإخراج يبدو مثل الملف الأصلي.
### **تصدير Microsoft Visio الرسم إلى ملف الصورة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToImage.vsd");

// Save Image file
diagram.Save(dataDir + "ExportToImage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}
```

من الممكن أيضًا حفظ صفحة معينة على الصورة ، بدلاً من حفظ المستند بأكمله:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportPageToImage.vsd");

// Save diagram as PNG
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.PNG);

// Save one page only, by page index
options.PageIndex = 0;

// Save resultant Image file
diagram.Save(dataDir + "ExportPageToImage_out.png", options);

{{< /highlight >}}
```