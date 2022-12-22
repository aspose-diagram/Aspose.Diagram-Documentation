---
title: Aspose.Diagram for .NET 22.10 ملاحظات الإصدار
type: docs
weight: 18
url: /ar/net/aspose-diagram-for-net-22-10-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for .NET 22.10.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52988|يتم عرض الرسم بجودة رديئة عند تصديره إلى تنسيق SVG|التعزيز|
|DIAGRAMNET-53002|فقد الارتباط عند التصدير إلى html باستخدام Aspose.Diagram|التعزيز|
|DIAGRAMNET-52983|خطأ في Diagram|حشرة|
|DIAGRAMNET-52984|قم بتغيير القيم في فئة VentureLicenser|حشرة|
|DIAGRAMNET-52993|فشل المحادثة من vsdx إلى svg|حشرة|
|DIAGRAMNET-52995|التطبيق: تحميل vsd يطرح استثناء|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف GetDisplayText في الشكل**
- احصل على النص المعروض على الواجهة

{{< highlight "java" >}}
String text = shape.GetDisplayText();
{{< /highlight >}}

### **يضيف InheritGeoms في الشكل**
- يحتوي على قيم Geoms للشكل الذي يرثه الشكل الرئيسي.

{{< highlight "java" >}}
int count = shape.InheritGeoms.Count;
{{< /highlight >}}