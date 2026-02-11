---
title: إعداد الخلايا في قسم الحدث من ورقة الشكل
type: docs
weight: 10
url: /ar/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

باستخدام Aspose.Diagram API ، يمكن للمطورين تحديد كيفية استجابة شكل لإجراءات مستخدم معينة عن طريق كتابة معادلات Visio التي تعالج الأحداث تلقائيًا. عندما يقوم المستخدم بتنفيذ أحد الإجراءات الموضحة أدناه ، يتم تقييم الصيغة الموجودة في خلية ورقة الشكل المقابلة.

- **النص** - عنصر حدث يتم تقييمه عند تغيير نص الشكل أو تكوين النص.
- **EventXFMod** - تم تغيير موضع الشكل أو حجمه أو اتجاهه على الصفحة.
- **EventDblClick** - تم النقر نقرًا مزدوجًا على الشكل.
- **EventDrop** يتم إنشاء مثيل جديد عن طريق لصق شكل أو نسخه أو سحبه ، أو عن طريق سحب الشكل الرئيسي وإفلاته.
- **EventMultiDrop** - عند إنشاء مثيلات جديدة متعددة عن طريق لصق شكل أو نسخه أو سحبه ، أو عن طريق سحب الشكل الرئيسي وإفلاته.
- **البيانات** - محجوزة للاستخدام في المستقبل.

{{% /alert %}} 
## **تعيين خلايا الحدث**
[حدث](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) تسمح class للمطورين بتعيين خلايا الأحداث في ورقة الشكل. يوضح موضوع التعليمات هذا كيف يمكن للمطورين تعيين الصيغ في خلايا الحدث:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SettingEventCells.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// get page
Page page = diagram.getPages().get(0);
// get shape id
long shapeId = page.addShape(3.0, 3.0, 0.36, 0.36, "Square");
// get shape
Shape shape = page.getShapes().getShape(shapeId);

// set event cells in the ShapeSheet
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");

// save diagram
diagram.save(dataDir + "Output_NET.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
