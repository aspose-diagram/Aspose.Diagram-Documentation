---
title: إعداد الخلايا في قسم الحدث من ورقة الشكل
type: docs
weight: 10
url: /ar/net/setting-cells-in-the-event-section-of-shapesheet/
description: إدارة خصائص الأحداث لملفات visio.
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد كيفية استجابة شكل لإجراءات مستخدم معينة عن طريق كتابة معادلات Visio التي تعالج الأحداث تلقائيًا. عندما يقوم المستخدم بتنفيذ أحد الإجراءات الأربعة الموضحة أدناه ، يتم تقييم الصيغة الموجودة في خلية ورقة الشكل المقابلة.

- **النص** - عنصر حدث يتم تقييمه عند تغيير نص الشكل أو تكوين النص.
- **EventXFMod** - تم تغيير موضع الشكل أو حجمه أو اتجاهه على الصفحة.
- **EventDblClick** - تم النقر نقرًا مزدوجًا على الشكل.
- **EventDrop** يتم إنشاء مثيل جديد عن طريق لصق شكل أو نسخه أو سحبه ، أو عن طريق سحب الشكل الرئيسي وإفلاته.
- **EventMultiDrop** - عند إنشاء مثيلات جديدة متعددة عن طريق لصق شكل أو نسخه أو سحبه ، أو عن طريق سحب الشكل الرئيسي وإفلاته.
- **البيانات** - محجوزة للاستخدام في المستقبل.

{{% /alert %}} 
## **تعيين خلايا الحدث**
[حدث](https://reference.aspose.com/diagram/net/aspose.diagram/event) تسمح class للمطورين بتعيين خلايا الأحداث في ورقة الشكل. يوضح موضوع التعليمات هذا كيف يمكن للمطورين تعيين الصيغ في خلايا الحدث:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
