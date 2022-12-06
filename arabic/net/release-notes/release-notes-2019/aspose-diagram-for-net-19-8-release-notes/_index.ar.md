---
title: Aspose.Diagram for .NET 19.8 ملاحظات الإصدار
type: docs
weight: 50
url: /ar/net/aspose-diagram-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 19.8](https://www.nuget.org/packages/Aspose.Diagram/19.8.0)

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-50334|إضافة دعم لأكواد VBA / وحدات الماكرو (إضافة - تحرير - حذف)|التعزيز|
|DIAGRAMNET-51083|إضافة دعم رسم المفتاح|التعزيز|
|DIAGRAMNET-51676|Visio إلى HTML - يحتوي الإخراج على اسم ملف فيه|التعزيز|
|DIAGRAMNET-50263|لا يمكن تعيين موقع نص الموصل كصيغ|حشرة|
|DIAGRAMNET-50284|VTX لتحويل HTML ، لا يتم الاحتفاظ بلون تعبئة الأشكال|حشرة|
|DIAGRAMNET-50432|VDX لتحويل PDF ، Diagram.setFontDirs تستخدم طريقة الخط الأول فقط على الكل diagram|حشرة|
|DIAGRAMNET-50463|تحويل VSDX إلى PDF ، تجسيد الأشكال الناقصة أو غير المكتملة|حشرة|
|DIAGRAMNET-51033|لا يتم الاحتفاظ بأشكال الشبكة عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMNET-51303|VSDX إلى PDF - تم تغيير لون النص على السطور المتصلة|حشرة|
|DIAGRAMNET-51663|يحدث استثناء غير معالج أثناء تحويل VSD إلى VSDX|حشرة|
|DIAGRAMNET-51664|تلف الملف بعد إزالة سمة غير مستخدمة|حشرة|
|DIAGRAMNET-51665|يتم عرض الصور على أنها X بعد إزالة السمات غير المستخدمة|حشرة|
|DIAGRAMNET-51667|أثناء إزالة الأنماط ، توجد مشكلة في الصورة فقط|حشرة|
|DIAGRAMNET-51668|من VISIO إلى JPG - صورة الإخراج ليست بالتنسيق الصحيح|حشرة|
|DIAGRAMNET-51671|أثناء إزالة الأشكال والأنماط الرئيسية غير المستخدمة ، توجد مشكلة في الصورة فقط|حشرة|
|DIAGRAMNET-51672|الصور المفقودة عند التحميل والحفظ|حشرة|
|DIAGRAMNET-51677|Visio إلى HTML - الارتباط في HTML الذي تم إنشاؤه لا يعمل|حشرة|
|DIAGRAMNET-51678|Visio to HTML - تنسيق التاريخ غير صحيح عند الحفظ بتنسيق HTML|حشرة|
|DIAGRAMNET-51679|Visio إلى PDF - العديد من أخطاء التنسيق في PDF|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف DrawSpline في الصفحة**
يوضح مقتطف الشفرة التالي كيفية رسم شريحة:

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{ new PointF(0, 0.3270758925347308f), 

                             new PointF(0.2926845121364643f, 0.3581517392187368f), 

                             new PointF(0.6526026522346893f, 0.4640748257705201f), 

                             new PointF(1f, 0.327075892534732f) };

                             diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **يضيف SaveTitle في HTMLSaveOptions**
يحدد مقتطف الشفرة التالي ما إذا كنت تريد حفظ العنوان أم لا:

{{< highlight "java" >}}

 Aspose.Diagram.Saving.HTMLSaveOptions options = new Aspose.Diagram.Saving.HTMLSaveOptions();

options.SaveTitle = false;

{{< /highlight >}}




