---
title: Aspose.Diagram for .NET 17.12 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-diagram-for-net-17-12-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.12](https://www.nuget.org/packages/Aspose.Diagram/17.12.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50016|أضف دعمًا لتكرار / استنساخ الشكل|التعزيز|
|DIAGRAMNET-50677|قم بتوفير API المفرد لتحويل شكل Visio إلى PDF|التعزيز|
|DIAGRAMNET-50678|قم بتوفير API المفرد لتحويل شكل Visio إلى HTML|التعزيز|
|DIAGRAMNET-50762|حدث خطأ التحليل لقيمة السمات الطويلة أثناء تكوين VDX diagram|حشرة|
|DIAGRAMNET-51401|الناتج VSDX - لا تعمل عناصر التحكم في الأشكال|حشرة|
|DIAGRAMNET-51402|VSDX للصورة - لا يتم الاحتفاظ بعنصر OLE|حشرة|
|DIAGRAMNET-51406|VSD للصورة - تظهر الحروف الإضافية|حشرة|
|DIAGRAMNET-51410|VSD إلى PDF - يبقى رقم الصفحة 4 في كل الصفحات|حشرة|
|DIAGRAMNET-51411|VSD للصورة - يبقى رقم الصفحة 4 في كل الصفحات|حشرة|
|DIAGRAMNET-51414|VSDX إلى PDF - فقدان محتوى الأشكال|حشرة|
|DIAGRAMNET-51415|VSDX إلى PDF - لون خلفية الأشكال غير صحيح|حشرة|
|DIAGRAMNET-51416|VSDX إلى HTML - لون خلفية الأشكال غير صحيح|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف نسخ العضو في فئة الشكل**
يأخذ العضو Copy مثيل الشكل الهدف ، كمعلمة لنسخ هذا الشكل.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
### **يضيف عضو ToPdf في فئة Shape**
يقوم عضو ToPdf بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf("e:\\out.pdf");

{{< /highlight >}}
### **إضافة عضو ToHTML في فئة Shape**
يقوم عضو ToHTML بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML("e:\\out.pdf", hs);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [انسخ شكل Visio إلى مثيل Shape آخر](/diagram/ar/net/add-2c-retrieve-2c-copy-and-read-visio-shape-data-html/#add-retrieve-copyandreadvisioshapedata-copyavisioshapetoanothershapeinstance)
1. [حوّل Visio إلى PDF](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-pdf/)
1. [حوّل Visio إلى HTML](https://docs.aspose.com/diagram/net/convert-a-visio-shape-to-html/)
