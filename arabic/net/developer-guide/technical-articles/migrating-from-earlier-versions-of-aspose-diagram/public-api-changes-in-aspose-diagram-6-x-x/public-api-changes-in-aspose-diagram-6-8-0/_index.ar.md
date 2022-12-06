---
title: API العام التغييرات في Aspose.Diagram 6.8.0
type: docs
weight: 10
url: /ar/net/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.6.0 إلى 6.8.0 ، والتي قد تهم مطوري الوحدة / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
## **أدخل عنصر تحكم ActiveX**
يمكن للمطورين إدراج عنصر تحكم ActiveX في Visio diagram. لقد أضفنا طريقة AddActiveXControl في[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) صف دراسي. الرجاء التحقق من مثال هذا الرمز:

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.Pages[0].AddActiveXControl(ControlType.Image, 1, 1, 1, 1);

// save diagram

diagram.Save(@"C:\temp\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

خطأ في عرض الماكرو 'code': تم تحديد قيمة غير صالحة للمعامل lang
## **قم بتعيين Color CheckBox of Layer**
يمكن للمطورين تعيين أو الحصول على Color CheckBox of Layer باستخدام Aspose.Diagram API. يرجى التحقق من مثال الكود هذا:

**C#**

{{< highlight "csharp" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// Get Visio page

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// Set Layer name

layer.Name.Value = "Layer1";

// Set Layer Visibility

layer.Visible.Value = BOOL.True;

// set the color checkbox of Layer

layer.IsColorChecked = BOOL.True;

// Add Layer to the particular page sheet

page.PageSheet.Layers.Add(layer);

// Get shape by ID

Shape shape = page.Shapes.GetShape(3);

// Assign shape to this new Layer

shape.LayerMem.LayerMember.Value = layer.IX.ToString();

// Save diagram

diagram.Save(@"c:\temp\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

خطأ في عرض الماكرو 'code': تم تحديد قيمة غير صالحة للمعامل lang
## **يضيف خاصية InheritFill في فئة الشكل**
يمكن للمطورين الحصول على خاصية التعبئة الموروثة أو تعيينها. لقد أضفنا خاصية InheritFill في فئة Shape. الرجاء التحقق من مثال هذا الرمز:

**C#**

{{< highlight "csharp" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page by ID

Page page = diagram.Pages.GetPage("Page-1");

// get shape by ID

Shape shape = page.Shapes.GetShape(1);

// get the fill formatting values

Console.WriteLine(shape.InheritFill.FillBkgnd.Value);

Console.WriteLine(shape.InheritFill.FillForegnd.Value);

Console.WriteLine(shape.InheritFill.FillPattern.Value);

{{< /highlight >}}

خطأ في عرض الماكرو 'code': تم تحديد قيمة غير صالحة للمعامل lang
