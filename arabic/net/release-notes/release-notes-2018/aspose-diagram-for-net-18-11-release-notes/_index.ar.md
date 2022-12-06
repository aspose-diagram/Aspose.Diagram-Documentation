---
title: Aspose.Diagram for .NET 18.11 ملاحظات الإصدار
type: docs
weight: 20
url: /ar/net/aspose-diagram-for-net-18-11-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.11](https://www.nuget.org/packages/Aspose.Diagram/18.11.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50410|MilestoneHelper - إضافة دعم محدد تنسيق سلسلة التاريخ المخصص|التعزيز|
|DIAGRAMNET-51568|أضف خيارًا لتعيين ViewBox في SaveOptions لـ SVG|التعزيز|
|DIAGRAMNET-51580|يقوم Aspose.Diagram بإنشاء SVG بإرشادات بينما MS Visio لا يقوم بذلك|التعزيز|
|DIAGRAMNET-51556|طريقة Shape.ToImage لا تولد صورًا صحيحة|حشرة|
|DIAGRAMNET-51557|تقوم طريقة Shape.ToImage بإرجاع صور فارغة في حالة وجود نسخة من الصفحة|حشرة|
|DIAGRAMNET-51570|طريقة Shape.ToImage لا تولد صورًا صحيحة|حشرة|
|DIAGRAMNET-51576|VSDX إلى PDF - كتل نصية مفقودة|حشرة|
|DIAGRAMNET-51578|VSDX لنتائج الصورة في StackOverFlowException|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف SVGFitToViewPort في SVGSaveOptions**
إذا كانت هذه الخاصية صحيحة ، فإن SVG الذي تم إنشاؤه سيكون مناسبًا لعرض المنفذ.

{{< highlight "java" >}}

 SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

SVGSaveOptions option = new SVGSaveOptions();

option.SVGFitToViewPort = true;

{{< /highlight >}}
### **يضيف ExportGuideShapes في RenderingSaveOptions**
يحدد ما إذا كنت بحاجة إلى تصدير أشكال الدليل أم لا.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.SVGSaveOptions o = new SVGSaveOptions();

o.ExportGuideShapes = false;

{{< /highlight >}}
### **يضيف DateFormatString في MilestoneHelper**
سلسلة الشكل DateFormat

{{< highlight "java" >}}

 milestoneHelper.DateFormatString = "yyyy/mm/dd";

{{< /highlight >}}
