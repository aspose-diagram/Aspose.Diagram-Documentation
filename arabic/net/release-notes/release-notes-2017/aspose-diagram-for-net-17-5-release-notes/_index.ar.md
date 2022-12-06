---
title: Aspose.Diagram for .NET 17.5 ملاحظات الإصدار
type: docs
weight: 80
url: /ar/net/aspose-diagram-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.5](https://www.nuget.org/packages/Aspose.Diagram/17.5.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51104|أضف دعمًا لخصائص الاستدارة ثلاثية الأبعاد للشكل|ميزة جديدة|
|DIAGRAMNET-51229|فتح وحفظ عملية VSDM يزيل SolutionXMLs|التعزيز|
|DIAGRAMNET-50283|VTX لتحويل HTML ، تأثير الخط المزدوج على عناصر نص الأشكال|حشرة|
|DIAGRAMNET-51195|عرض غير صحيح لأيقونة مغلف عند حفظ VDX إلى SVG|حشرة|
|DIAGRAMNET-51196|محاذاة نص غير صحيحة عند حفظ VDX إلى SVG|حشرة|
|DIAGRAMNET-51225|استرداد قيمة تقويم غير صحيحة لبيانات الشكل لـ VSDM|حشرة|
|DIAGRAMNET-51226|الحفظ في دفق HTML لا يدمج الموارد الخارجية|حشرة|
|DIAGRAMNET-51227|لا يمكن تعيين قيمة حفظ الوقت لـ VSDM|حشرة|
|DIAGRAMNET-51228|يتم إزاحة عناصر النص عند تعيين بيانات الشكل في VSDM|حشرة|
|DIAGRAMNET-51234|لا يمكن إزالة وإضافة نفس الاسم الرئيسي في VSDM|حشرة|
|DIAGRAMNET-51235|تقوم عملية فتح وحفظ VSDM بإزالة ملف vbaProjectSignature.bin|حشرة|
|DIAGRAMNET-51236|فتح وحفظ عملية VSDM تغييرات ملف XML الحل|حشرة|
|DIAGRAMNET-51237|لا يمكن حفظ قيم Del و NoQuickDrag لـ Geoms في VSDM|حشرة|
|DIAGRAMNET-51238|اضبط قيمة TimeSaved عند حفظ رسم Visio|حشرة|
|DIAGRAMNET-51239|تقوم عملية فتح وحفظ VSDM بإزالة جزء العلاقة من XML للحل|حشرة|
|DIAGRAMNET-51240|نص مُزاح عند تحويل VSD إلى PDF|حشرة|
|DIAGRAMNET-51242|لا يمكن إضافة بيانات الشكل إلى الأشكال المختلفة في VSDM|حشرة|
|DIAGRAMNET-51243|لم يتم حفظ قيمة UFEV لخلية المستخدم بشكل صحيح في VSDM|حشرة|
|DIAGRAMNET-51244|خطأ xml للصفحة مكرر في نسخ صفحات من رسمين VSDM|حشرة|
|DIAGRAMNET-51247|يتم أيضًا تضمين منطقة غير مطبوعة عند تحويل VSD إلى PDF|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **إضافة عضو ThreeDFormat في فئة الشكل**
تسمح فئة ThreeDFormat للمطورين باسترداد أو تعيين خصائص الاستدارة ثلاثية الأبعاد للشكل.

{{< highlight "java" >}}

 // Load diagram

Diagram diagram = new Diagram(@"c:\temp\3DShape_Rotation.vsdx");

// get page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);

// set RotationXAngle property, 

// all other properties are added in ThreeDFormat class

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

// save diagram to VSDX format

diagram.Save(@"c:\temp\3DShape_Rotation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [تعديل خصائص الاستدارة ثلاثية الأبعاد في ورقة الأشكال](/diagram/ar/net/3d-rotation-effects-in-a-visio-drawing/#id-3drotationeffectsinavisiodrawing-set3drotationpropertiesinshapesheet)
