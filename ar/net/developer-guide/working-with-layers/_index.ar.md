---
title: العمل مع الطبقات
type: docs
weight: 130
url: /ar/net/working-with-layers/
description: يشرح هذا القسم كيفية إضافة أو الحصول على معلومات الطبقة في شكل visio مع Aspose.Diagram.
---
## **تكوين كائنات الشكل مع الطبقات في Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يسمح بتكوين كائنات الشكل بطبقات في Microsoft Office Visio diagram. يمكن أن ينتمي كل شكل إلى طبقات متعددة حتى يتمكن المطورون من إدارة الأشكال لتناسب احتياجات المستخدم النهائي. ال[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يقدم كائن الفئة خاصية LayerMember التي تسمح بإضافة وإزالة كائنات الشكل من وإلى الطبقات في رسم Visio. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:
### **تكوين نموذج برمجة كائنات الشكل**
يساعد الجزء التالي من التعليمات البرمجية على إضافة خصائص كائن الشكل وإزالتها ونقلها.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name.ToLower() == "shape1")
    {
        // Add shape1 in first two layers. Here "0;1" are indexes of the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0;1";
    }
    else if (shape.Name.ToLower() == "shape2")
    {
        // Remove shape2 from all the layers
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "";
    }
    else if (shape.Name.ToLower() == "shape3")
    {
        // Add shape3 in first layer. Here "0" is index of the first layer
        LayerMem layer = shape.LayerMem;
        layer.LayerMember.Value = "0";
    }
}
// Save diagram
diagram.Save(dataDir + "ConfigureShapeLayers_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **أضف طبقة جديدة في Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يسمح للمطورين بإضافة طبقات جديدة لتنظيم فئات مخصصة من الأشكال ، ثم تعيين الأشكال لتلك الطبقات برمجيًا. ال[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) يقدم class طريقة Add التي تسمح بإضافة ملف[طبقة](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) في الرسم Visio. يمكن للمطورين تعيين خصائص الطبقة عن طريق تهيئة كائن الفئة الخاص بها.
### **إضافة عينة برمجة طبقة**
يساعد الجزء التالي من التعليمات البرمجية على إضافة كائنات الطبقة.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Initialize a new Layer class object
Layer layer = new Layer();
// Set Layer name
layer.Name.Value = "Layer1";
// Set Layer Visibility
layer.Visible.Value = BOOL.True;
// Set the color checkbox of Layer
layer.IsColorChecked = BOOL.True;
// Add Layer to the particular page sheet
page.PageSheet.Layers.Add(layer);

// Get shape by ID
Shape shape = page.Shapes.GetShape(3);
// Assign shape to this new Layer
shape.LayerMem.LayerMember.Value = layer.IX.ToString();
// Save diagram
diagram.Save(dataDir + "AddLayer_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **استرجع كل الطبقات من Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يتيح للمطورين الوصول إلى الطبقات الموجودة في Visio diagram. The[ورقة الصفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) ممتلكات[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) تسمح الفئة باسترداد قائمة الطبقات المتاحة من Visio diagram باستخدام[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) صف دراسي.
### **استرجاع عينة برمجة الطبقات**
يساعد الجزء التالي من التعليمات البرمجية في الحصول على قائمة الطبقات.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Layer layer in page.PageSheet.Layers)
{
    Console.WriteLine("Name: " + layer.Name.Value);
    Console.WriteLine("Visibility: " + layer.Visible.Value);
    Console.WriteLine("Status: " + layer.Status.Value);
}

{{< /highlight >}}

