---
title: Aspose.Diagram for .NET 22.5 ملاحظات الإصدار
type: docs
weight: 23
url: /ar/net/aspose-diagram-for-net-22-5-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram for .NET 22.5.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52802|الصيغة / القيمة لا تقوم بتحديث الحقول|التعزيز|
|DIAGRAMNET-52803|VSDX إلى HTML: ملف الإخراج لا يتم حفظه بطريقة Async حتى يتم تنفيذ البرنامج بالكامل|التعزيز|
|DIAGRAMNET-52793|API لا يعمل مع إصدار 22.4 ترخيص صالح|حشرة|
|DIAGRAMNET-52806|مسافة بادئة مغيرة في PDF من VSDX|حشرة|
|DIAGRAMNET-52807|تتم إزالة النص الموجود في الجدول أثناء تحويل ملف .vsdx إلى pdf [CONT.]|حشرة|
|DIAGRAMNET-52808|مشكلة في تحويل VSDX إلى PDF [CONT.]|حشرة|
|DIAGRAMNET-52810|Visio الأشكال المحفوظة كصور خاطئة|حشرة|
|DIAGRAMNET-52811|الأشكال مفقودة بعد حفظ Visio إلى HTML|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **يضيف DisplayValue في الحقل**
- الحصول على قيمة السلسلة المنسقة لهذا الحقل.

{{< highlight "java" >}}
String str = shape.Fields[0].DisplayValue;
{{< /highlight >}}

### **يضيف InheritParas في الشكل**
- يحتوي على الفقرات الخاصة بالشكل الذي يرثه النمط الأصل والشكل الرئيسي

{{< highlight "java" >}}
ParaCollection paras = shape.InheritParas;
Console.WriteLine(paras[0].HorzAlign.Value);
{{< /highlight >}}