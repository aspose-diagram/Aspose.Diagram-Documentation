---
title: Aspose.Diagram for .NET 17.9 ملاحظات الإصدار
type: docs
weight: 40
url: /ar/net/aspose-diagram-for-net-17-9-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.9](https://www.nuget.org/packages/Aspose.Diagram/17.9.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51261|أضف دعمًا لتحويل منطقة معينة من الرسم إلى صورة|التعزيز|
|DIAGRAMNET-51350|إضافة دعم لاسترداد الشكل بالاسم|التعزيز|
|DIAGRAMNET-51351|أضف دعمًا لاسترداد الشكل من التعليق التوضيحي|التعزيز|
|DIAGRAMNET-51295|VSDX إلى SVG - تدني جودة الإنتاج SVG|حشرة|
|DIAGRAMNET-51309|يحدث DiagramException عند حفظ الملف VSDX|حشرة|
|DIAGRAMNET-51331|VSDM إلى SVG - تم إزاحة عناصر النص لأعلى|حشرة|
|DIAGRAMNET-51333|VSDM إلى SVG - عرض غير صحيح للرموز الدائرية|حشرة|
|DIAGRAMNET-51339|VSDX إلى SVG - اقتطاع النص من الجانب الأيمن لكل صورة|حشرة|
|DIAGRAMNET-51340|ترتيب التعليقات غير صحيح|حشرة|
|` ` DIAGRAMNET-51342|حدث خطأ في نفاد الذاكرة بعد استخدام طريقة "AddComment" وحفظ الملف على Steam|حشرة|
|DIAGRAMNET-51344|VSDX إلى PDF - حدث خطأ خارج النطاق في الوسيطة|حشرة|
|DIAGRAMNET-51345|لا يتم حذف التعليق مع الشكل|حشرة|
|DIAGRAMNET-51346|VSDM إلى SVG - تم تخفيض جودة الشعار|حشرة|
|DIAGRAMNET-51347|VSDM إلى SVG - تم تخفيض جودة الشعار|حشرة|
|DIAGRAMNET-51353|لا يمكن إضافة تعليق آخر في صفحة Visio|حشرة|
|DIAGRAMNET-51354|لا يمكن تحرير التعليقات في صفحة Visio|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف عضو GetShape في ShapeCollection**
يسمح باسترداد شكل بالاسم.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// retrieve page by name

Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by name

Shape shape = page.Shapes.GetShape("name");

{{< /highlight >}}
### **يضيف عضو ShapeID في التعليق التوضيحي**
يسمح بتتبع شكل التعليق.

{{< highlight "java" >}}

 string dataDir = @"C:\temp\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get the annotation by index

Annotation annotation = diagram.Pages.GetPage("Page-1").PageSheet.Annotations[1];

// get shape Id

Console.WriteLine(annotation.ShapeID);

{{< /highlight >}}
### **يضيف منطقة في RenderingSaveOptions**
يسمح بتحويل منطقة المستطيل المحددة لرسم Visio.

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\\test.vsdx");

ImageSaveOptions Options = new ImageSaveOptions(SaveFileFormat.PNG);

// specify region

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save("e:\\area.png", Options);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [تحويل المساحة المحددة للصفحة Visio إلى صورة](https://docs.aspose.com/diagram/net/working-with-images/#convert-specified-area-of-the-visio-page-to-an-image)
1. [تباعد تلقائي لمجموعة من الأشكال في صفحة Visio](/diagram/ar/net/auto-space-a-collection-of-shapes-in-the-visio-page/)
