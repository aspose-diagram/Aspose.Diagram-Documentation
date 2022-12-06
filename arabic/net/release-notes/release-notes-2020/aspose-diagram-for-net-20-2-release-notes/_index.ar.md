---
title: Aspose.Diagram for .NET 20.2 ملاحظات الإصدار
type: docs
weight: 60
url: /ar/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51747|تغييرات الملف بعد تحويل Visio vsd-> vsdx|التعزيز|
|DIAGRAMNET-51750|إضافة علامة "HasHiddenInfo"|التعزيز|
|DIAGRAMNET-51748|أضف PNG إلى Diagram - ضاعت الشفافية|حشرة|
|DIAGRAMNET-51749|حدث خطأ أثناء حفظ المستند Visio|حشرة|
|DIAGRAMNET-51751|VSDX إلى PNG - تظهر الصورة الإضافية|حشرة|
|DIAGRAMNET-51752|VSDX إلى PNG - تظهر مسافة إضافية|حشرة|
|DIAGRAMNET-51753|VSDX إلى PNG - يتغير موضع الأيقونات|حشرة|
|DIAGRAMNET-51754|VSDX إلى PNG - تم تغيير موضع أيقونة علامة الاستفهام|حشرة|
|DIAGRAMNET-51762|يختلف ملف PDF الذي تم إنشاؤه عن الإدخال Visio diagram|حشرة|
|DIAGRAMNET-51763|VSDX إلى PNG - المعلومات مفقودة في الإخراج|حشرة|
## ` `**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
` ` فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على for .NET Aspose.Diagram. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على منتدى الدعم Aspose.Diagram.
### **تمت إضافة تكبير الصفحة في ImageSaveOptions**
- يحدد ما إذا كان سيتم تكبير الصفحة أم لا

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **تمت إضافة HasHiddenInfo في Diagram**
- الإشارة إلى ما إذا كان diagram يحتوي على معلومات مخفية.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




