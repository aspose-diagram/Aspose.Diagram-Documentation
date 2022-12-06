---
title: Aspose.Diagram for .NET 17.7 ملاحظات الإصدار
type: docs
weight: 60
url: /ar/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51204|تم تغيير حجم ورق الطابعة بعد حفظ diagram.|التعزيز|
|DIAGRAMNET-51230|قيم غير صحيحة لهوامش الصفحة.|التعزيز|
|DIAGRAMNET-51274|أضف دعمًا لإدراج التعليقات على مستوى الشكل.|التعزيز|
|DIAGRAMNET-51297|إدخال VDX - قراءة غير صحيحة لـ SolutionXML.|التعزيز|
|DIAGRAMNET-51061|أشكال مفقودة عند تحويل VST إلى PNG.|حشرة|
|DIAGRAMNET-51262|تم إزاحة عناصر النص عند تحويل VSDM إلى SVG.|حشرة|
|DIAGRAMNET-51276|VSD إلى SVG - كل الأيقونات غير مرئية بشكل صحيح.|حشرة|
|DIAGRAMNET-51277|VSDM إلى SVG - ظل الأشكال مفقود.|حشرة|
|DIAGRAMNET-51279|حرف مفقود عند تحويل VSD إلى PDF.|حشرة|
|DIAGRAMNET-51282|تلف بعض ملفات vdx بعد الحفظ.|حشرة|
|الرسم البياني - 51284-|يحدث DiagramException عند تحميل ملف vsdx.|حشرة|
|DIAGRAMNET-51285|VSD إلى PNG - جميع عناصر النص مفقودة.|حشرة|
|DIAGRAMNET-51286|VSD إلى PNG - العرض الجزئي للشكل.|حشرة|
|DIAGRAMNET-51288|خطأ في قيمة اللون غير صالح عند تحويل VSDX إلى PNG.|حشرة|
|DIAGRAMNET-51289|لا تعرض أيقونة التعليقات على مستوى الصفحة النص.|حشرة|
|DIAGRAMNET-51290|Aspose.Diagram خطأ في طريقة SetWidth.|حشرة|
|DIAGRAMNET-51291|الناتج VSDX - تخطيط غير صحيح عند ضبط الخطوط المتصلة بشكل مستقيم.|حشرة|
|DIAGRAMNET-51292|الناتج VSDX - تم وضع عنصر النص الخاص بالخطوط المتصلة في غير مكانه.|حشرة|
|DIAGRAMNET-51293|VSDX إلى SVG - تظهر علامة إضافية مع الأشكال.|حشرة|
|DIAGRAMNET-51294|VSDM إلى SVG - تظهر علامة إضافية مع الأشكال.|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **تمت إضافة طريقة AddComment في فئة الصفحة**
طريقة AddComment المحملة بشكل زائد ، والتي يتم عرضها بواسطة فئة الصفحة تأخذ مثيل فئة الشكل وسلسلة نصية للتعليق.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [أضف تعليقًا على مستوى الشكل في رسم Visio](/diagram/ar/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
