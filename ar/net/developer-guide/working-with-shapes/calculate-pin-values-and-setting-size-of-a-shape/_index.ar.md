---
title: حساب قيم الدبوس وتحديد حجم الشكل
type: docs
weight: 60
url: /ar/net/calculate-pin-values-and-setting-size-of-a-shape/
description: يشرح هذا القسم كيفية حساب قيم PinX و PinY للشكل الفرعي مع Aspose.Diagram.
---
## **حساب قيم PinX و PinY للشكل الفرعي**
 إذا كان الشكل عبارة عن عقدة فرعية لشكل المجموعة ، فإن xform الخاص به هو إحداثي نسبي لشكله الأصلي ولكنه ليس تنسيقًا مطلقًا في[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page). إذا طلب المستخدم الحصول على الإحداثيات المطلقة ، فإن نموذج التعليمات البرمجية هذا يساعد.

يمكن تحويل نقطة محددة في الإحداثيات المحلية إلى إحداثيات رئيسية من خلال تطبيق التحويلات التالية بالترتيب التالي:

1. اطرح قيمة الخاصية LocPinX لعنصر Cell_Type من إحداثي x.
1. اطرح قيمة الخاصية LocPinY الخاصة بنوع الخلية من الإحداثي ص.
1. قم بعكس النقطة حول المحور y إذا كانت قيمة خاصية FlipX في Cell_Type تساوي واحدًا.
1. عكس النقطة حول المحور x إذا كانت قيمة الخاصية FlipY في Cell_Type تساوي واحدًا.
1. قم بتدوير النقطة عكس اتجاه عقارب الساعة حول الأصل بقيمة خاصية Angle الخاصة بالنوع Cell_Type.
1. أضف قيمة PinX Cell_Type إلى إحداثيات x.
1. أضف قيمة PinY Cell_Type إلى الإحداثي y.
### **حساب عينة برمجة PinX و PinY**
استخدم الكود التالي في تطبيق .NET لحساب قيم PinX و PinY لشكل فرعي باستخدام Aspose.Diagram for .NET API.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **ضبط ارتفاع الشكل وعرضه**
 ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) تسمح لك الفئة بالتحكم في حجم الشكل عن طريق تحديد ارتفاع الشكل وعرضه باستخدام أساليب SetHeight و SetWidth.

 أساليب SetHeight و SetWidth ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)فئة ، دعم تغيير حجم الشكل مع السيد ، بدون الرئيسي أو في شكل شكل مجموعة. تعيين أمثلة التعليمات البرمجية في هذه المقالة الارتفاع والعرض لتغيير حجم الشكل على الصفحة.

عملية ضبط الارتفاع والعرض هي:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. اضبط ارتفاع الشكل.
1. تعيين عرض الشكل.
1. احفظ diagram.
### **تعيين الارتفاع والعرض عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية تعيين ارتفاع الشكل وعرضه. يبحث الكود عن مستطيل لاسم الشكل ، بمعرف الشكل 1 ، ويضبط الارتفاع والعرض على أنهما مزدوجان.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

