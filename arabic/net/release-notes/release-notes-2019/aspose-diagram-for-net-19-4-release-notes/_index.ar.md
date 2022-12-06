---
title: Aspose.Diagram for .NET 19.4 ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/aspose-diagram-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.4](https://www.nuget.org/packages/Aspose.Diagram/19.4.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51602|تعرض كائن XSLX المضمن للتلف بعد التلاعب به|التعزيز|
|DIAGRAMNET-51625|تتم إزالة بيانات Excel الخارجية الموجودة في ملفات .vsdx عند إعادة حفظ Diagram|التعزيز|
|DIAGRAMNET-51626|API لا يعالج بيانات Excel|التعزيز|
|DIAGRAMNET-51627|استخراج بيانات الشكل على أساس صيغة Dependson|التعزيز|
|DIAGRAMNET-51629|يبدو أن توسيع الصفحة لتلائم الرسم لا يعمل|التعزيز|
|DIAGRAMNET-51176|يتم تغيير شريط عنوان التدرج عند تحويل VSDM إلى SVG|حشرة|
|DIAGRAMNET-51404|VSD للصورة - لون الشكل غامق|حشرة|
|DIAGRAMNET-51473|VDX إلى PDF - لون الخلفية غير الصحيح|حشرة|
|DIAGRAMNET-51475|VSDX إلى PDF - يتم تجسيد التدرجات في الاتجاه المعاكس|حشرة|
|DIAGRAMNET-51616|Visio إلى PDF - يظهر التدرج مقلوبًا في ملف PDF الناتج|حشرة|
|DIAGRAMNET-51630|VSDX إلى HTML - لون الخلفية للأشكال غير موجود في المخرجات|حشرة|
|DIAGRAMNET-51631|VSDX إلى PDF - لون خلفية الأشكال غير موجود في المخرجات|حشرة|
|DIAGRAMNET-51632|VSD إلى SVG - تعذر تحويل كائن من النوع "" لكتابة "" حدث الاستثناء|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف RemoveHiddenInfoItem التعداد**
يحدد إزالة المعلومات المخفية لـ diagram.
### **يضيف RemoveHiddenInfoItem في Diagram**
إزالة المعلومات غير المستخدمة.

{{< highlight "java" >}}

diagram.RemoveHiddenInformation((int)(RemoveHiddenInfoItem.Shapes | RemoveHiddenInfoItem.Masters));

{{< /highlight >}}
