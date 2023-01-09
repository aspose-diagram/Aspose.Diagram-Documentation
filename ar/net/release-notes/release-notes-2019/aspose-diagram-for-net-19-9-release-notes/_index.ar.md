---
title: Aspose.Diagram for .NET 19.9 ملاحظات الإصدار
type: docs
weight: 40
url: /ar/net/aspose-diagram-for-net-19-9-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 19.9.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51683|Visio إلى HTML - الارتباط الذي تم إنشاؤه HTML لا يعمل بشكل صحيح|التعزيز|
|DIAGRAMNET-51684|أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة ، توجد مشكلة في الصورة فقط|التعزيز|
|DIAGRAMNET-51711|غير قادر على إضافة وحدات الماكرو بعد التحويل|التعزيز|
|DIAGRAMNET-50383|تصغير الحجم Visio diagram|حشرة|
|DIAGRAMNET-51682|احصل على نمط الخط من Diagram|حشرة|
|DIAGRAMNET-51685|Visio إلى SVG - حدث استثناء|حشرة|
|DIAGRAMNET-51686|Visio إلى PNG - يحتوي ملف الإخراج على صور وأشكال غير مرغوب فيها|حشرة|
|DIAGRAMNET-51687|Visio إلى PDF - لون خلفية النص غائب في الإخراج PDF|حشرة|
|DIAGRAMNET-51688|Visio إلى PDF - يختلف لون إطارات الأشكال في الإخراج|حشرة|
|DIAGRAMNET-51689|Visio إلى JPG - صورة الإخراج ليست في التنسيق الصحيح|حشرة|
|DIAGRAMNET-51691|Visio إلى PDF - بعض الأشكال غير صحيحة|حشرة|
|DIAGRAMNET-51692|Visio إلى PDF - بعض الأشكال غير صحيحة|حشرة|
|DIAGRAMNET-51693|Visio إلى PDF - بعض الأشكال غير صحيحة|حشرة|
|DIAGRAMNET-51694|Visio إلى PDF - بعض الأشكال غير صحيحة|حشرة|
|DIAGRAMNET-51697|Visio إلى PDF - بعض الأشكال غير صحيحة|حشرة|
|DIAGRAMNET-51700|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51702|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51706|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51707|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51708|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51709|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
|DIAGRAMNET-51710|Visio إلى PDF - بعض الأشكال / الخطوط غير صحيحة|حشرة|
### **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

|**يتغيرون**|**غاية**|**عينة**|
|:- |:- |:- |
| إضافة**IsBold** إلى Aspose.Shape.Char|توضيح ما إذا كان الخط غامقًا أم لا.|<p>Aspose.Diagram.Char ch = shape.Chars [0] ؛</p><p>الفصل هو جريء</p>|
| إضافة**إيطالي** إلى Aspose.Shape.Char|الإشارة إلى ما إذا كان الخط مائلًا أم لا.|<p>Aspose.Diagram.Char ch = shape.Chars [0] ؛</p><p>الفصل الإيطالي</p>|
| إضافة**هو تسطير** إلى Aspose.Shape.Char|الإشارة إلى ما إذا كان الخط هو "تسطير".|<p>Aspose.Diagram.Char ch = shape.Chars [0] ؛</p><p>الفصل</p>|
| إضافة**IsDoubleUnderline** إلى Aspose.Shape.Char|الإشارة إلى ما إذا كان الخط مسطرًا مزدوجًا أم لا|<p>Aspose.Diagram.Char ch = shape.Chars [0] ؛</p><p>الفصل</p>|
| إضافة**IsStrikethrough** إلى Aspose.Shape.Char|الإشارة إلى ما إذا كان الخط يتوسطه خط أم لا.|<p>Aspose.Diagram.Char ch = shape.Chars [0]</p><p>الفصل</p>|
| إضافة**IsDoubleStrikethrough** إلى Aspose.Shape.Char|توضيح ما إذا كان الخط يتوسطه خط مزدوج|<p>Aspose.Diagram.Char ch = shape.Chars [0] ؛</p><p>ch.IsDoubleStrikethrough</p>|

