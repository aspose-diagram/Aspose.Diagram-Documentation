---
title: Aspose.Diagram for .NET 18.10 ملاحظات الإصدار
type: docs
weight: 30
url: /ar/net/aspose-diagram-for-net-18-10-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51527|تضيع الصور بعد التحويل VSDM إلى SVG|التعزيز|
|DIAGRAMNET-51532|VSD إلى PDF - ظل الصورة غير صحيح|التعزيز|
|DIAGRAMNET-51536|تمت إزالة ظل الشكل بعد التحويل VSDX إلى SVG|التعزيز|
|DIAGRAMNET-51544|تتم إزالة التسطير من النص بعد تحويل VSDM إلى SVG|التعزيز|
|DIAGRAMNET-51558|تطبيق Getter لـ Shape.ConnectorsType|التعزيز|
|DIAGRAMNET-51520|VDX إلى HTML - تظهر خطوط إضافية في الإخراج|حشرة|
|DIAGRAMNET-51521|يتم تغيير الخط الموجود في diagram بعد حفظ VSD كـ VSDX|حشرة|
|DIAGRAMNET-51523|VSDX إلى SVG - رؤوس الأسهم مفقودة|حشرة|
|DIAGRAMNET-51524|VSDM إلى SVG - ظهرت Blue Crosses في ملف الإخراج|حشرة|
|DIAGRAMNET-51525|يتغير شكل القرار من الماس إلى المربع بينما يتم التحويل من VSDM إلى SVG|حشرة|
|DIAGRAMNET-51528|يتغير شكل القرار من الماس إلى المربع بينما يتم التحويل من VSDM إلى SVG|حشرة|
|DIAGRAMNET-51529|VSDM إلى SVG - تحويل الخطوط المنقطة إلى سطور ممتلئة|حشرة|
|DIAGRAMNET-51531|يتم تحويل الأشكال إلى الجانب الأيمن بعد تحويل VSDX إلى SVG|حشرة|
|DIAGRAMNET-51533|ظهرت الصليب الأحمر بعد تحويل VISIO إلى SVG|حشرة|
|DIAGRAMNET-51534|ظهرت النقطة الحمراء في الزاوية اليسرى السفلية من الشكل|حشرة|
|DIAGRAMNET-51538|فقدت الصور بعد التحويل VSDX إلى PDF|حشرة|
|DIAGRAMNET-51541|أصبح النص غير مرئي بعد التحويل VSDX إلى SVG|حشرة|
|DIAGRAMNET-51542|تم حذف النص بعد التحويل VSDX إلى SVG|حشرة|
|DIAGRAMNET-51543|تم تغيير تنسيق الوقت والتاريخ بعد VSDM إلى SVG|حشرة|
|DIAGRAMNET-51545|VSDX إلى SVG - يتم تغليف النص في الإخراج|حشرة|
|DIAGRAMNET-51546|VSDX إلى SVG - يتم تغليف النص في الإخراج|حشرة|
|DIAGRAMNET-51547|VSDX إلى SVG - يتم تغليف النص في الإخراج|حشرة|
|DIAGRAMNET-51548|VSDX إلى SVG - يتم تغليف النص في الإخراج|حشرة|
|DIAGRAMNET-51551|تعذر الحصول على لون النسق الصحيح للأشكال|حشرة|
|DIAGRAMNET-51552|تظهر رؤوس الأسهم المعكوسة في تحويل SVG|حشرة|
|DIAGRAMNET-51559|مشكلة في تغيير حجم النص أثناء تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51560|تصبح خطوط الموصل رقيقة بعد التحويل إلى SVG|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **تمت إضافة InheritLine في الشكل**
يحتوي على قيم تنسيق الخط للشكل الذي يرثه النمط الأصل والشكل الرئيسي.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **تمت إضافة GetConnectorsType في الشكل**
الحصول على نوع الموصلات

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}

