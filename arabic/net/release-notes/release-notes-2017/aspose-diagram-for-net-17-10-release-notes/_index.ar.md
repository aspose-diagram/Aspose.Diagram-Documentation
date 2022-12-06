---
title: Aspose.Diagram for .NET 17.10 ملاحظات الإصدار
type: docs
weight: 30
url: /ar/net/aspose-diagram-for-net-17-10-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.10](https://www.nuget.org/packages/Aspose.Diagram/17.10.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51349|أضف دعمًا لتحويل رسم إلى صورة بنفس مساحة PDF|التعزيز|
|DIAGRAMNET-51352|الوصول إلى الملفات المضمنة|التعزيز|
|DIAGRAMNET-51085|تُفقد الصيغ ضمن علامة تبويب عناصر التحكم في ورقة الأشكال عند الحفظ في VSDX|حشرة|
|DIAGRAMNET-51094|احتفظ بالإعدادات الافتراضية ضمن علامة تبويب التحكم عند وضع شكل شبه منحرف|حشرة|
|DIAGRAMNET-51355|VSDX إلى PDF - تم وضع العناصر النصية في غير مكانها|حشرة|
|DIAGRAMNET-51356|VSDX إلى HTML - تم وضع العناصر النصية في غير مكانها|حشرة|
|DIAGRAMNET-51357|فتح وحفظ الإجراء VSDX - التاريخ المفقود وتحرير سمات التاريخ للتعليقات التوضيحية|حشرة|
|` ` DIAGRAMNET-51358|حدث خطأ مؤشر فارغ عند تحميل رسم VSDX|حشرة|
|DIAGRAMNET-51359|خطأ في قائمة مؤلف العنصر بعد تحميل VSDX|حشرة|
|DIAGRAMNET-51361|VSDX إلى VDX - خط النص غير الصحيح للشكل|حشرة|
|DIAGRAMNET-51363|روتين الفتح والحفظ VSDX - يتحول قسم علامات التبويب إلى علامة إغلاق ذاتيًا|حشرة|
|DIAGRAMNET-51365|VSD إلى PNG - تخطيط غير صحيح للأشكال|حشرة|
|DIAGRAMNET-51367|VSD استيراد الرسم - خطأ في عنصر رئيسي|حشرة|
|DIAGRAMNET-51368|VSD إلى PNG - حدث خطأ تجاوز|حشرة|
|DIAGRAMNET-51369|VSD إلى PDF - عناصر نصية في غير مكانها في الأسفل|حشرة|
|DIAGRAMNET-51371|VSDX إلى VSDX - تم إضافة عناصر نصية إضافية|حشرة|
|DIAGRAMNET-51373|يفتقد إجراء فتح وحفظ رسم VSDX لخط نص آسيوي|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف SameAsPdfConversionArea في ImageSaveOptions**
تحدد ما إذا كان سيتم حفظ المنطقة بنفس طريقة حفظ المساحة PDF.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

Aspose.Diagram.Saving.ImageSaveOptions opts = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

opts.SameAsPdfConversionArea = true;

{{< /highlight >}}
