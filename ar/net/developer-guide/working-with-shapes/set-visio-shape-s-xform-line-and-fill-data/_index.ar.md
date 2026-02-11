---
title: قم بتعيين Visio شكل XForm و Line و Fill Data
type: docs
weight: 20
url: /ar/net/set-visio-shape-s-xform-line-and-fill-data/
description: يشرح هذا القسم كيفية تعيين نمط الشكل بما في ذلك بيانات الخط وملء البيانات بـ Aspose.Diagram.
---
## **ضبط بيانات XForm**
 عنصر XForm هو جزء من Microsoft Visio مخطط XML. يحدد XForm موضع الأشكال ، على سبيل المثال العرض والارتفاع والدوران وما إذا كان الشكل قد انعكس. ال[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) الممتلكات التي يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة ، يدعم كائن Aspose.Diagram.XForm. يمكن استخدام الخاصية XForm لاسترداد بيانات XForm للشكل أو تحديثها. تعمل أمثلة التعليمات البرمجية في هذه المقالة على تغيير قيم PinX (إحداثيات س) و PinY (إحداثيات ص) لتحريك الأشكال على الصفحة.

عملية تحديث بيانات XForm هي:

1. قم بتحميل diagram. # ابحث عن شكل معين # قم بتحديث بيانات XForm للشكل.
1. احفظ diagram.
### **عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تحديث بيانات XForm للشكل. يبحث الكود عن عملية أسماء الأشكال ، بمعرف الشكل 1 ، ويضبط إحداثياته X و Y على 5.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.XForm.PinX.Value = 5;
        shape.XForm.PinY.Value = 5;
    }
}
// Save diagram
diagram.Save(dataDir + "SetXFormdata_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **قم بتعيين Visio بيانات خط الشكل**
يمكن تنسيق الأشكال بعدة طرق. توضح هذه المقالة كيفية تحديد سمات السطر.

Microsoft Visio يتيح للمستخدمين تنسيق السطور بعدة طرق. Aspose.Diagram for .NET يدعم:

- الوزن: سمك الخط.
- اللون: تعيين لون خط الشكل.
- شفافية لون الخط: اضبط شفافية لون خط الشكل بالنسبة المئوية.
- النمط: يحدد ما إذا كان الخط متصلًا أم متقطعًا أم له نمط آخر.
- التقريب: نصف قطر الزوايا.
- أسهم البداية والنهاية: تحدد ما إذا كان السطر يحتوي على أسهم أم لا.
- أحجام أسهم البداية والنهاية: قم بتعيين أحجام الأسهم.
- الغطاء: تقريب الخط ينتهي.
### **تغيير لون الخط والوزن ونوع الشرطة والشفافية والتقريب ونوع السهم وحجم السهم لحد الشكل**
 ال[خط](http://www.aspose.com/api/net/diagram/aspose.diagram/line) الممتلكات التي يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)فئة ، تدعم كائن Aspose.Diagram.Line. يمكن استخدام هذه الخاصية لاسترداد بيانات خط الشكل أو تحديثها.
#### **عينة برمجة بيانات الخط**
يقوم الجزء التالي من التعليمات البرمجية بتحديث بيانات خط الشكل.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set line dash type by index
shape.Line.LinePattern.Value = 4;
// Set line weight, defualt in inch
shape.Line.LineWeight.Value = 2;
// Set color of the shape's line
shape.Line.LineColor.Ufe.F = "RGB(95,108,53)";
// Set line rounding, default in inch
shape.Line.Rounding.Value = 0.3125;
// Set line caps
shape.Line.LineCap.Value = BOOL.True;
// Set line color transparency in percent
shape.Line.LineColorTrans.Value = 50;

/* add arrows to the connector or curve shapes */
// Select arrow type by index
shape.Line.BeginArrow.Value = 4;
shape.Line.EndArrow.Value = 4;
// Set arrow size 
shape.Line.BeginArrowSize.Value = ArrowSizeValue.Large;
shape.Line.EndArrowSize.Value = ArrowSizeValue.Large;

// Save the Visio
diagram.Save(dataDir + "SetLineData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **قم بتعيين Visio بيانات تعبئة الشكل**
 يمكن تنسيق الأشكال بعدة طرق. يصف هذا الموضوع كيفية تحديد تعبئة الشكل. Microsoft Office Visio يتيح للمستخدمين تنسيق التعبئة بطرق مختلفة. ال[يملأ](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) فئة Aspose.Diagram for .NET API تدعم الإعداد:

- ألوان الخلفية والمقدمة.
- الشفافية.
- أنماط التعبئة.
- الظلال.
### **ضبط قيم التعبئة**
 خاصية Fill ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) الطبقة ، يدعم[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) هدف. يمكن استخدام الخاصية Fill لاسترداد بيانات تعبئة الشكل أو تحديثها.
#### **تعبئة نموذج لبرمجة البيانات**
يقوم مقتطف التعليمات البرمجية التالي بتحديث بيانات تعبئة الشكل. تبحث الشفرة عن شكل يسمى مستطيل ، بمعرف الشكل 1 ، وتعيين خلفية التعبئة وألوان المقدمة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetFillData.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "rectangle" && shape.ID == 1)
    {
        shape.Fill.FillBkgnd.Value = diagram.Pages[1].Shapes[0].Fill.FillBkgnd.Value;
        shape.Fill.FillForegnd.Value = "#ebf8df";
    }
}
// Save diagram
diagram.Save(dataDir + "SetFillData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **استرجع بيانات التعبئة الموروثة لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات التعبئة الموروثة لشكل Visio أو تعيينها. الخاصية InheritFill ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ، تحتوي على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwObliqueAngle.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetX.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetY.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwScaleFactor.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwType.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgnd.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwForegnd.Value);
Console.WriteLine(shape.InheritFill.ShdwForegndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwPattern.Value);

{{< /highlight >}}

