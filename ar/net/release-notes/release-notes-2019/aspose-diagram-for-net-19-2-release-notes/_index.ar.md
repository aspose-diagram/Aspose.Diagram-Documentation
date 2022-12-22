---
title: Aspose.Diagram for .NET 19.2 ملاحظات الإصدار
type: docs
weight: 110
url: /ar/net/aspose-diagram-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.2](https://www.nuget.org/packages/Aspose.Diagram/19.2.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50009|يختلط شكل القلب عند تصدير VSD رسمًا بتنسيق ملف PDF|التعزيز|
|DIAGRAMNET-50010|VSD إلى PDF يقوم بتصدير خطوط متعرجة متعددة بنقطة متزامنة بدلاً من خط منحنى واحد|التعزيز|
|DIAGRAMNET-51257|أضف دعمًا لخط NUBRS عند تصدير الرسم|التعزيز|
|DIAGRAMNET-51611|تعذر الحصول على Prop.Prompt.Value بشكل صحيح|التعزيز|
|DIAGRAMNET-50355|يتم تصدير الخطوط المنحنية كخطوط مستقيمة|حشرة|
|DIAGRAMNET-50702|تصدير VSDX إلى PDF - تتحول الوصلات المنحنية إلى مستقيمة|حشرة|
|DIAGRAMNET-51348|VSDX إلى PDF - عرض غير صحيح للحروف|حشرة|
|DIAGRAMNET-51399|VSD إلى PNG - يتم تحويل الخط المنحني إلى خط مستقيم|حشرة|
|DIAGRAMNET-51448|VSD إلى PNG - القطع الناقص مفقود حول كلمة شبكة|حشرة|
|DIAGRAMNET-51472|VSD إلى PDF - يتم تصدير الخطوط المنحنية كخطوط مستقيمة|حشرة|
|DIAGRAMNET-51507|VSDX إلى PNG - الأشكال البيضاوية المعبأة مفقودة في الإخراج|حشرة|
|DIAGRAMNET-51508|VSDX إلى SVG - الأشكال البيضاوية المعبأة مفقودة في الإخراج|حشرة|
|DIAGRAMNET-51537|VSDX إلى SVG - تصبح الموصلات المنحنية موصلات مستقيمة عندما يتم تحويل VSDX إلى PDF|حشرة|
|DIAGRAMNET-51540|تم تغيير حواف الشكل كمربع بعد التحويل|حشرة|
|DIAGRAMNET-51577|VISIO إلى SVG - الإخراج غير صحيح|حشرة|
|DIAGRAMNET-51592|تتغير الخطوط المنحنية إلى خطوط مستقيمة أثناء التحويل|حشرة|
|DIAGRAMNET-51600|تصبح الخطوط المستقيمة مسامير عند حفظ diagram كتنسيق آخر|حشرة|
|DIAGRAMNET-51604|VSDX إلى PDF خطأ في التحويل - علامات حذف سوداء|حشرة|
|DIAGRAMNET-51605|تحديث المراجع API وإضافة تفاصيل حول طريقة Shape.SetAngle ()|حشرة|
|DIAGRAMNET-51610|VSDX إلى SVG - لا يتم تحويل النص بالخط الصحيح|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **أضف InheritProps في الشكل**
يحتوي على دعائم الشكل التي يرثها الشكل الرئيسي.

{{< highlight "java" >}}

  foreach (Aspose.Diagram.Prop prop in shape.InheritProps)

{

    Console.WriteLine(prop.Name);

    Console.WriteLine(prop.Label.Value);

    Console.WriteLine(prop.Prompt.Value);

    Console.WriteLine(prop.Type.Value.ToString());

    Console.WriteLine(prop.Value.Val);

    Console.WriteLine(prop.Format.Value);

}

{{< /highlight >}}
