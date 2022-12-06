---
title: Aspose.Diagram for .NET 19.1 ملاحظات الإصدار
type: docs
weight: 120
url: /ar/net/aspose-diagram-for-net-19-1-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.1](https://www.nuget.org/packages/Aspose.Diagram/19.1.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51082|إضافة دعم رسم Polyline|التعزيز|
|DIAGRAMNET-51084|أضف دعمًا لرسم أشكال بيزيير|التعزيز|
|DIAGRAMNET-51231|اعرض التعليقات عند الحفظ كصورة أو بتنسيق HTML|التعزيز|
|DIAGRAMNET-51597| VISIO to SVG - استخدام عناصر المستطيل<path> علامة بدلاً من<Rect>|التعزيز|
|DIAGRAMNET-50764|قراءة VSDX تفتقد إلى قيمة اللون للأشكال المختلفة|حشرة|
|DIAGRAMNET-51336|إصلاح المشكلات في إصدار Aspose.Diagram for .NET/Java|حشرة|
|DIAGRAMNET-51343|الناتج VSDX - لم يتم تغيير حجم الشكل|حشرة|
|DIAGRAMNET-51579|قفل القراءة موجود بعد استدعاء طريقة Save ()|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف DrawPolyline في الصفحة**
عملية رسم الخطوط المتعددة.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2), new PointF(3.79949292203676f, 0) };

diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **يضيف DrawBezier في الصفحة**
عملية رسم بيزير.

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{new PointF(1, 1), new PointF(2, 2)};

diagram.Pages[0].DrawBezier(1, 1, 2, 2, ps);

{{< /highlight >}}
### **يضيف IsExportComments في ImageSaveOptions و HTMLSaveOptions**
يحدد ما إذا كان يلزم تصدير التعليقات أم لا.

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions io = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

io.IsExportComments = true;

Aspose.Diagram.Saving.HTMLSaveOptions htmlo = new Aspose.Diagram.Saving.HTMLSaveOptions();

htmlo.IsExportComments = false;

{{< /highlight >}}
### **يضيف ExportElementAsRectTag في SVGSaveOptions**
يحدد ما إذا كنت بحاجة إلى تصدير عناصر مستطيلة كعلامة مستقيمة أم لا.

{{< highlight "java" >}}

 var SVGso = new Aspose.Diagram.Saving.SVGSaveOptions();

SVGso.ExportGuideShapes = false;

SVGso.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;

SVGso.SVGFitToViewPort = true;

SVGso.ExportElementAsRectTag = true;

{{< /highlight >}}
