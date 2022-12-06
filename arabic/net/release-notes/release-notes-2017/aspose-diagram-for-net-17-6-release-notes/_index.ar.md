---
title: Aspose.Diagram for .NET 17.6 ملاحظات الإصدار
type: docs
weight: 70
url: /ar/net/aspose-diagram-for-net-17-6-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.6](https://www.nuget.org/packages/Aspose.Diagram/17.6.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51264|يكون ظل الأشكال أسود عند تحويل VSDM إلى SVG|التعزيز|
|DIAGRAMNET-51270|لا يمكن رؤية شكل VSDX في عارض Visio|التعزيز|
|DIAGRAMNET-51273|عرض الشكل غير صحيح في عارض Visio 2013|التعزيز|
|DIAGRAMNET-51249|المظهر غير الصحيح للخط المنحني الذي يربط VSDM|حشرة|
|DIAGRAMNET-51250|تمت إضافة قوس أيسر إضافي في النص عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51251|تم تقليل حجم الأيقونة إلى إصدار أقدم عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51253|لون النص غير صحيح والحدود في الأشكال عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51255|تم سحق صورة في الأسفل عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51258|روتين فتح وحفظ VSDM - تم تغيير طول الجدران|حشرة|
|DIAGRAMNET-51259|روتين فتح وحفظ VSDM - تم تغيير طول الجدران|حشرة|
|DIAGRAMNET-51260|حدث خطأ في نطاق خارج الفهرس عند استدعاء أسلوب التخطيط للفئة Diagram|حشرة|
|DIAGRAMNET-51263|تظهر علامة لون أحمر إضافية عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51265|يتم تغيير خط نص العنوان عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51266|يتم تقليل حجم صورة الخلفية لتحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51267|يتم إرجاع حجم الرمز إلى إصدار أقدم عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51268|يسترجع قيمة الشفافية غير الصحيحة لصورة من رسم VSDM|حشرة|
|DIAGRAMNET-51269|أضف الحماية الافتراضية|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **إضافة عضو RefreshData في فئة الشكل**
تعمل طريقة RefreshData لمثيل فئة Shape على تحديث بيانات الشكل ، بما في ذلك XForm و TextXForm و Connection و Geom ، بعد تغيير نص الشكل أو غيره.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set PinX and PinY values

shape.XForm.PinX.Value = 5;

shape.XForm.PinY.Value = 5;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
