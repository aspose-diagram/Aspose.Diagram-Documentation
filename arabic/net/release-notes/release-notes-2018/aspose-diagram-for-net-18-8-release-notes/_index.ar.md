---
title: Aspose.Diagram for .NET 18.8 ملاحظات الإصدار
type: docs
weight: 50
url: /ar/net/aspose-diagram-for-net-18-8-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 18.8](https://www.nuget.org/packages/Aspose.Diagram/18.8.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51500|مشكلة التقديم للصورة|التعزيز|
|DIAGRAMNET-51504|أضف دعمًا لإنشاء مراجع جديد|التعزيز|
|DIAGRAMNET-50953|يتم إزاحة عناصر النص عند تحويل VSDX إلى PNG|حشرة|
|DIAGRAMNET-51122|الموضع غير الصحيح لعناصر النص عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51123|يتم إزاحة نص الأشكال عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51408|VSD للصورة - تتداخل الحروف مع السطر|حشرة|
|DIAGRAMNET-51499|Diagram. يطرح أسلوب الحفظ OutOfMemoryException|حشرة|
|DIAGRAMNET-51501|تتداخل الأشكال في ملف VDX|حشرة|
|DIAGRAMNET-51505|النقاط مفقودة في ملف PDF الذي تم إنشاؤه|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **يضيف المراجع**
{{< highlight "java" >}}

             Reviewer viewer = new Reviewer();

            viewer.Name.Value = "test";

            viewer.ReviewerID.Value = 3;

{{< /highlight >}}




