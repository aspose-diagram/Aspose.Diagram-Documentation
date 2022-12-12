﻿---
title: Aspose.Diagram for .NET 22.4 ملاحظات الإصدار
type: docs
weight: 24
url: /ar/net/aspose-diagram-for-net-22-4-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram for .NET 22.4.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52015|تذكرة استمرار # DIAGRAMNET-51995 - إصدارات مع ملفات Aspose.Diagram و Skyline Datamine|التعزيز|
|DIAGRAMNET-52707|لا تؤدي التغييرات التي تم إجراؤها على صيغة / قيمة ورقة الشكل إلى إجراء تغييرات في الخلايا التابعة|التعزيز|
|DIAGRAMNET-50345|من VSDX إلى PDF ، لون خلفية غير صحيح للأشكال|حشرة|
|DIAGRAMNET-50954|مشاكل التنسيق في عرض جدول وزر اختيار عند تحويل VSDX إلى PNG|حشرة|
|DIAGRAMNET-52708|تحويل موضع النص إلى svg|حشرة|
|DIAGRAMNET-52739|تنسيق النقاط الحساسة للثقافة|حشرة|
|DIAGRAMNET-52759|تتم إزالة النص الموجود في الجدول أثناء تحويل ملف .vsdx إلى pdf|حشرة|
|DIAGRAMNET-52762|VSDX إلى PDF - لم يتم تحويل الصورة|حشرة|
|DIAGRAMNET-52779|لا يتم تحجيم القطع الناقصة أثناء التحويل من Visio إلى SVG|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **يضيف GetPureText في الشكل**
- احصل على سلسلة نصية للشكل.

{{< highlight "java" >}}
String text = shape.GetPureText();
{{< /highlight >}}
