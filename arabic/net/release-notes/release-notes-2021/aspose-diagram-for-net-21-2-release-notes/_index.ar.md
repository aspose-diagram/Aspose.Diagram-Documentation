---
title: Aspose.Diagram for .NET 21.2 ملاحظات الإصدار
type: docs
weight: 11
url: /ar/net/aspose-diagram-for-net-21-2-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 21.2.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51986|أضف طريقة الرسم centerDrawing الموجودة في صفحة interop visio|التعزيز|
|DIAGRAMNET-51987|تنفيذ طريقة للحصول على ActivePage|التعزيز|
|DIAGRAMNET-51978|تحويل VSD إلى VSDX - غير قادر على فتح الإخراج في MS Visio|حشرة|
|DIAGRAMNET-51980|"حدث خطأ عام في GDI +." استثناء عند التقديم إلى ملف HTML VSDX|حشرة|
|DIAGRAMNET-51981|تحويل VSDX إلى PDF - الأشكال سوداء في ملف pdf الناتج|حشرة|
|DIAGRAMNET-51985|تحويل VSDX إلى VSDX/VDX: ألوان الشكل تتغير إلى التدرج بعد الحفظ|حشرة|
|DIAGRAMNET-51989|Visio إلى HTML - حد غريب في المخرجات|حشرة|

## ` `**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
` ` فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على for .NET Aspose.Diagram. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على منتدى الدعم Aspose.Diagram.
### **تمت إضافة ActivePage في Diagram**
- تحدد الصفحة النشطة

{{< highlight "java" >}}

Page page = diagram.ActivePage;

{{< /highlight >}}
### **يضيف CenterDrawing في الشكل**
- توسيط الشكل فيما يتعلق بمدى الصفحة



{{< highlight "java" >}}

shape.CenterDrawing()

{{< /highlight >}}
### **يضيف DrawLine في الصفحة**
- عملية رسم خط واحد.



{{< highlight "java" >}}

 diagram.Pages[0].DrawLine(0,0,1,1);

{{< /highlight >}}



