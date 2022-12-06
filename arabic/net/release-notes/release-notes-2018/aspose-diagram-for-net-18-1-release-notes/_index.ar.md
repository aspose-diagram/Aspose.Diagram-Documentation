---
title: Aspose.Diagram for .NET 18.1 ملاحظات الإصدار
type: docs
weight: 120
url: /ar/net/aspose-diagram-for-net-18-1-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.1](https://www.nuget.org/packages/Aspose.Diagram/18.1.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50494|إضافة دعم لتكرار / استنساخ صفحة diagram|التعزيز|
|DIAGRAMNET-51057|زر الأمر مفقود بعد إزالة صفحة من VSDM|التعزيز|
|DIAGRAMNET-51422|VSDX إلى PDF - يتم تجاهل الظلال في أشكال العمليات|التعزيز|
|DIAGRAMNET-50467|VSD إلى PDF التحويل ، شعار الشركة في غير مكانه|حشرة|
|DIAGRAMNET-50469|من VSD إلى PDF ، يكون نص شكل الراديو أعلى قليلاً من المعتاد|حشرة|
|DIAGRAMNET-51199|لم تتم محاذاة نص العنوان عند حفظ VSDM إلى SVG|حشرة|
|DIAGRAMNET-51388|مشاكل تتعلق بتحميل ملفات vsdx وحفظها|حشرة|
|DIAGRAMNET-51398|VSD إلى PNG - موضع النص غير صحيح|حشرة|
|DIAGRAMNET-51407|VSD إلى JPEG - تم وضع العناصر النصية في غير مكانها|حشرة|
|DIAGRAMNET-51419|لم يتم تغيير حجم الأشكال بشكل صحيح في ملف vsdx|حشرة|
|DIAGRAMNET-51420|VSDX تلف الملف بعد التحميل والحفظ|حشرة|
|DIAGRAMNET-51421|VSDX إلى PDF - لون خط غير صحيح للنص|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف نسخ العضو في فئة الصفحة**
يأخذ العضو Copy مثيل الصفحة الهدف ، كمعامل لاستنساخ هذه الصفحة.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy diagram

newPage.Copy(diagram.Pages[0]);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [قم بنسخ Visio صفحة إلى نسخة صفحة أخرى](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#copy-visio-page-to-another-page-instance)
