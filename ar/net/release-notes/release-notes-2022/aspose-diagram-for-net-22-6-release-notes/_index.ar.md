---
title: Aspose.Diagram for .NET 22.6 ملاحظات الإصدار
type: docs
weight: 22
url: /ar/net/aspose-diagram-for-net-22-6-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram for .NET 22.6.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52826|رابط مقطوع عند حفظ VSDM إلى PDF|التعزيز|
|DIAGRAMNET-52851|تفقد بعض الأشكال منحنىها بعد التحويل إلى svg|التعزيز|
|DIAGRAMNET-52858|جودة الصورة في HTML|التعزيز|
|DIAGRAMNET-52825|تصدير لمشكلة HTML|حشرة|
|DIAGRAMNET-52832|Visio إلى PDF/SVG - تم تغيير موضع النص المستدير|حشرة|
|DIAGRAMNET-52840|تم تعتيم العناصر الموجودة في معاينة HTML|حشرة|
|DIAGRAMNET-52842|صفحة الاحتواء التلقائي لا تناسب تلقائي|حشرة|
|DIAGRAMNET-52849|الصور النقطية لم يتم تصغيرها بعد التحويل|حشرة|
|DIAGRAMNET-52852|VSD فتح خطأ - Aspose.Diagram.DiagramException|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **يضيف الدقة في HTMLSaveOptions**
- الحصول على دقة وضوح HTML التي تم إنشاؤها أو تعيينها ، بالنقاط في البوصة.

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.Resolution = 96;
{{< /highlight >}}
