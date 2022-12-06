---
title: Aspose.Diagram for .NET 18.3 ملاحظات الإصدار
type: docs
weight: 100
url: /ar/net/aspose-diagram-for-net-18-3-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.3](https://www.nuget.org/packages/Aspose.Diagram/18.3.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50147|VSD لتحويل XPS ، يتم تكوين الصفحات الفارغة بصور حمراء متصالبة|التعزيز|
|DIAGRAMNET-51431|أضف طريقة MoveTo لمجموعة الصفحات|التعزيز|
|DIAGRAMNET-50424  |VSDX لتحويل PDF ، تكون الأيقونة فوق النص|حشرة|
|DIAGRAMNET-50459|VSDX لتحويل PDF ، رمز الشكل في غير مكانه من موضعه الأصلي|حشرة|
|DIAGRAMNET-50460|VSDX لتحويل PDF ، رمز الشكل في غير مكانه من موضعه الأصلي|حشرة|
|DIAGRAMNET-50674|لا يتم حفظ كافة موارد HTML في المسار المخصص|حشرة|
|DIAGRAMNET-51403|VSD للصورة - رؤوس الأسهم في غير مكانها|حشرة|
|DIAGRAMNET-51427|الناتج VSDX - لا تعمل عناصر التحكم في الأشكال|حشرة|
|DIAGRAMNET-51429|إصلاح عنوان URL لصفحة المنتج فوق معرض NuGet|حشرة|
|DIAGRAMNET-51432|إجراء فتح وحفظ VSDX لا يحافظ على خلية الخط|حشرة|
|DIAGRAMNET-51433|لا يمكن استرداد كافة أسماء الأشكال من رسم VSDX|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف عضو MoveTo في فئة الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [انقل موضع الصفحة في الرسم Visio](https://docs.aspose.com/diagram/net/retrieve-get-copy-and-insert-a-page/#move-page-position-in-the-visio-drawing)
