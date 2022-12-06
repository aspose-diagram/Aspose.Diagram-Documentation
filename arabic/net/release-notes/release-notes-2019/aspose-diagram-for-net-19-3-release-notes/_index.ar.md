---
title: Aspose.Diagram for .NET 19.3 ملاحظات الإصدار
type: docs
weight: 100
url: /ar/net/aspose-diagram-for-net-19-3-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.3](https://www.nuget.org/packages/Aspose.Diagram/19.3.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50930|إضافة دعم لاسترداد دلائل الخطوط الشائعة على أنظمة التشغيل|التعزيز|
|DIAGRAMNET-51614|احصل على كل قيمة الدعائم للشكل|التعزيز|
|DIAGRAMNET-50214|تحويل VSD إلى PDF - تصبح الخطوط المنحنية خطاً مستقيماً|حشرة|
|DIAGRAMNET-50240|تحويل من VSD إلى PDF - مخطط خاطئ للموصلات الديناميكية|حشرة|
|DIAGRAMNET-50703|تصدير VSDX إلى PDF - موصل ديناميكي مفقود|حشرة|
|DIAGRAMNET-50704|تصدير VSD إلى PDF - تتحول أشكال نوع Meta إلى رموز فوضوية|حشرة|
|DIAGRAMNET-51535|VSDM إلى SVG - تم تغيير الخط من Sans إلى Serif في SVG|حشرة|
|DIAGRAMNET-51574|VSDX إلى PNG - تم تقديم بعض الأشكال بشكل غير صحيح في الإخراج PNG|حشرة|
|DIAGRAMNET-51608|التفاف النص لا يعمل كما هو متوقع|حشرة|
|DIAGRAMNET-51609|يتم إزاحة الأشكال إلى الجانب الأيسر عند نسخ Diagram إلى شريحة PowerPoint|حشرة|
|DIAGRAMNET-51617|Visio إلى PDF - لا تظهر القيم المستندة إلى البيانات الخارجية بشكل صحيح|حشرة|
|DIAGRAMNET-51619|Visio إلى PDF - تاريخ / وقت / مسافة غير صحيحة في PDF|حشرة|
|DIAGRAMNET-51621|Visio إلى PDF - صورة الخلفية مشوهة والصفحة الإضافية موجودة في PDF|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف GetDefaultFontDir في Diagram**
احصل على مسار مجلد الخطوط الافتراضية

{{< highlight "java" >}}

  string str =  diagram.GetDefaultFontDir();

{{< /highlight >}}
