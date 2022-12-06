---
title: Aspose.Diagram for .NET 17.8 ملاحظات الإصدار
type: docs
weight: 50
url: /ar/net/aspose-diagram-for-net-17-8-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for .NET 17.8](https://www.nuget.org/packages/Aspose.Diagram/17.8.0).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMNET-51295|VSDX إلى SVG - تدني جودة الإنتاج SVG.|التعزيز|
|DIAGRAMNET-51298|SVGSaveOptions - إضافة دعم للتحكم في مستوى ضغط الصور النقطية.|التعزيز|
|DIAGRAMNET-51300|أضف دعمًا لربط الأشكال بفهرس الاتصال.|التعزيز|
|DIAGRAMNET-50577|تحويل VSDX إلى PDF ، يكون نص الشكل الدائري في غير مكانه - I.|حشرة|
|DIAGRAMNET-50582|تحويل VSDX إلى HTML ، يكون نص الشكل الدائري في غير مكانه - I.|حشرة|
|DIAGRAMNET-50601|VSDX إلى PDF ، يكون نص الشكل الدائري في غير مكانه - II.|حشرة|
|DIAGRAMNET-50606|VSDX إلى HTML ، يكون نص الشكل الدائري في غير مكانه - II.|حشرة|
|DIAGRAMNET-51197|لا يتم عرض أشكال مثلث التحذير بشكل صحيح في حفظ VSDM إلى SVG.|حشرة|
|DIAGRAMNET-51245|تم إزاحة عناصر النص عند تحويل VSD إلى PDF.|حشرة|
|DIAGRAMNET-51246|تم تطبيق خطوط غير صحيحة على النص عند تحويل VSD إلى PDF.|حشرة|
|DIAGRAMNET-51296|VSDM إلى SVG - تم اقتطاع الصورة.|حشرة|
|DIAGRAMNET-51301|VSDX إلى PDF - تم تغيير لون النص في السطور المتصلة.|حشرة|
|DIAGRAMNET-51302|VSDX إلى PDF - عناصر بيانية مفقودة.|حشرة|
|DIAGRAMNET-51304|VSDX إلى PDF - عرض غير كامل لمخطط التدفق.|حشرة|
|DIAGRAMNET-51305|VSDX إلى PDF - عناصر بيانية مفقودة.|حشرة|
|DIAGRAMNET-51306|VSDX إلى PDF - تم تغيير لون النص في السطور المتصلة.|حشرة|
|DIAGRAMNET-51307|VSDX إلى PDF - عناصر بيانية مفقودة.|حشرة|
|DIAGRAMNET-51313|يؤدي فتح وحفظ الإجراء الخاص برسم VSDX إلى إنشاء ملف مخرجات تالف.|حشرة|
|DIAGRAMNET-51314|VSDX إلى SVG - وضع غير صحيح للنص.|حشرة|
|DIAGRAMNET-51317|VSDX إلى PDF - نص السطور المتصلة مفقود.|حشرة|
|DIAGRAMNET-51318|VSDX إلى PDF - النص المنسق الغامق لأشكال المستطيل مفقود.|حشرة|
|DIAGRAMNET-51319|VSDM إلى SVG - نتج عن العملية الحسابية خطأ تجاوز.|حشرة|
|DIAGRAMNET-51320|خطأ في عنصر الشكل أثناء تحميل VSDM.|حشرة|
|DIAGRAMNET-51323|VSDM إلى SVG - جميع الخطوط المتصلة مفقودة.|حشرة|
|DIAGRAMNET-51324|VSDM إلى SVG - نمط حد غير صحيح ولون حدود لأشكال مختلفة.|حشرة|
|DIAGRAMNET-51326|يصدر بعد إضافة تعليقين على الشكل.|حشرة|
|DIAGRAMNET-51327|مشكلة بعد استخدام طريقة "AddComment" عند إضافة تعليقات على أشكال مختلفة.|حشرة|
|DIAGRAMNET-51328|Aspose Diagram يقوم باستقبال الشكل للوثيقة بشكل غير صحيح.|حشرة|
|DIAGRAMNET-51330|VSDM إلى SVG - تمت إضافة نص علامة مائية إضافية.|حشرة|
|DIAGRAMNET-51332|VSDM إلى SVG - عرض غير صحيح لأيقونة.|حشرة|
|DIAGRAMNET-51334|VSDM إلى SVG - نص مزاح في الزاوية اليمنى العليا.|حشرة|
|DIAGRAMNET-51335|VSDM إلى SVG - عرض غير صحيح لصورة الخلفية.|حشرة|
|DIAGRAMNET-51337|VSD إلى HTML - تنسيق غير صالح لخطأ سلسلة الإدخال.|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for .NET. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف عضو الجودة في فئة SVGSaveOptions**
يحصل أو يحدد قيمة تحدد جودة الصور التي تم إنشاؤها.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.Quality = 100;

// save drawing in the SVG format

diagram.Save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **يضيف أسلوب ConnectShapesViaConnectorIndex في فئة الصفحة**
يسمح بتوصيل الأشكال باستخدام فهارس الاتصال.

{{< highlight "java" >}}

 string dataDir = @"c:\temp\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Aspose.Diagram.Shape shape1 = diagram.Pages[0].Shapes.GetShape(1);

Aspose.Diagram.Shape shape2 = diagram.Pages[0].Shapes.GetShape(2);

// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.Pages[0].ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

// save drawing

diagram.Save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [استخدم فهارس الاتصال لتوصيل الأشكال](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/#use-connection-indexes-to-connect-shapes)
1. [استخدام SVG حفظ الخيارات](https://docs.aspose.com/diagram/net/save-visio-document/)
