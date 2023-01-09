---
title: Aspose.Diagram for .NET 20.10 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-diagram-for-net-20-10-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 20.10.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51891|Visio إلى JPG - يستغرق API وقتًا طويلاً للتحويل|التعزيز|
|DIAGRAMNET-51902|لا يتم دعم ملفات Visio بإصدارات أقل من 11 استثناء عند فتح VSS|التعزيز|
|DIAGRAMNET-51906|تصدير VSDX إلى PDF: مشاكل في عرض الخط والصورة والأبعاد|التعزيز|
|DIAGRAMNET-51929|VSD إلى SVG التحويل: تحويلات المصفوفة في ملف الإخراج SVG|التعزيز|
|DIAGRAMNET-51931|Visio إلى PDF-API يستهلك قدرًا كبيرًا من الذاكرة ويستغرق وقتًا طويلاً|التعزيز|
|DIAGRAMNET-51936|[تابع] Visio إلى PDF - API يستهلك قدرًا كبيرًا من الذاكرة ويستغرق وقتًا طويلاً|التعزيز|
|DIAGRAMNET-51881|2 موضع تسميات غير صحيحة|حشرة|
|DIAGRAMNET-51907|حدث خطأ عام في GDI + استثناء يحدث عند تقديم ملف VSDX|حشرة|
|الرسم البياني - 51926-|Aspose.Diagram 20.9: NullReferenceException عند التحويل VDX إلى PNG|حشرة|
|DIAGRAMNET-51928|تحويل VSD إلى SVG: بعض النصوص والأسهم في نهاية السطور مفقودة|حشرة|
|DIAGRAMNET-51932|أنماط الأشكال المفقودة بعد تحويل vsd -> vsdx|حشرة|
|DIAGRAMNET-51933|توقف التدرج اللوني تنسيق غير مطابق لمعيار svg|حشرة|
|DIAGRAMNET-51934|مرجع كائن لم يتم تعيين إلى مثيل كائن.' عند حفظ أشكال VSS لملف معين|حشرة|
|DIAGRAMNET-51940|2 موضع تسميات غير صحيحة|حشرة|

## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**  ##
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

 * تمت إضافة IsExportScaleInMatrix في SVGSaveOptions - يحدد ما إذا كنت بحاجة إلى نطاق تصدير في المصفوفة أم لا.
```
Aspose.Diagram.Saving.SVGSaveOptions o = new Aspose.Diagram.Saving.SVGSaveOptions();
o.IsExportScaleInMatrix = false;
```
