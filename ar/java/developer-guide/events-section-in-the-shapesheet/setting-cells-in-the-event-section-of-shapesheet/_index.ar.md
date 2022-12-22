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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-eventsection-SettingEventCells-SettingEventCells.java" >}}
