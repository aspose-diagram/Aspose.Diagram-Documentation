---
title: Aspose.Diagram for .NET 22.3 ملاحظات الإصدار
type: docs
weight: 25
url: /ar/net/aspose-diagram-for-net-22-3-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram for .NET 22.3.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-52667|شكل.RefreshShape () لا يعمل لعكس قيمة BeginY المتغيرة|التعزيز|
|DIAGRAMNET-52668|الهندسة لا تظهر نتائج الصيغة غير محدثة|التعزيز|
|DIAGRAMNET-52655|التطبيق: تحميل vsd من الإصدار القديم والحفظ في pdf يطرح استثناء|حشرة|
|DIAGRAMNET-52661|لا يوجد مثال على إضافة العلامة المائية إلى visio في التوثيق|حشرة|
|DIAGRAMNET-52663|الكشف عن أنماط الخط المخصصة للشكل باستخدام المفتاح الفارغ|حشرة|
|DIAGRAMNET-52666|Visio لتحويل PDF - مشكلة في رسومات البيانات [تابع]|حشرة|
|DIAGRAMNET-52684|استثناء عند التصدير إلى HTML|حشرة|
|DIAGRAMNET-52685|استثناء عند التصدير إلى HTML|حشرة|
|DIAGRAMNET-52692|Diagram الحفظ في MemoryStream باستخدام تنسيق PDF يطرح System.NullReferenceException|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف AddText في الصفحة**
- يضيف نص مع تعريف PinX و PinY.

{{< highlight "java" >}}
double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
double width = page.PageSheet.PageProps.PageWidth.Value;
double height = page.PageSheet.PageProps.PageHeight.Value;
Shape shape = page.AddText(pinx, piny, width, height, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
