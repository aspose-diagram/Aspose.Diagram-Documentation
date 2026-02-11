---
title: العمل مع الخلايا المعرفة من قبل المستخدم
type: docs
weight: 150
url: /ar/net/working-with-user-defined-cells/
description: يشرح هذا القسم كيفية قراءة الخلايا المعرفة من قبل المستخدم لأشكال visio مع Aspose.Diagram.
---
## **اقرأ الخلايا المعرفة من قبل المستخدم للأشكال Visio**
 يقوم المستخدمون بإدراج الحقول النصية في الأشكال لعرض معلومات إضافية.**خلايا معرّفة من قبل المستخدم** هو فرع واحد من هذه الحقول ويستخدم هذا الفرع المعلومات التي تم إدخالها في خلية القيمة الخاصة بقسم الخلايا المعرفة من قبل المستخدم في ورقة الشكل الخاصة بالشكل. يمكن للمطورين إدراج وقراءة جميع الخلايا المحددة من قبل المستخدم باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **استرجع حقول الخلايا المعرفة من قبل المستخدم**
 مجموعة المستخدمين مكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة تدعم Aspose.Diagram.User object. يمكن استخدام هذه الخاصية لقراءة الخلايا المعرفة من قبل المستخدم لشكل Visio كما هو متاح في قسم الخلايا المعرفة من قبل المستخدم في ورقة الشكل.

![ما يجب القيام به: image_بديل_نص](working-with-user-defined-cells_1.png)
#### **استرجاع عينة برمجة الخلايا**
يسمح الجزء التالي من التعليمات البرمجية للمطورين بقراءة حقول الخلايا التي يحددها المستخدم.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(1);
// Extract user defined cells of the shape
foreach (User user in shape.Users)
{
    Console.WriteLine(user.Name + ": " + user.Value.Val);
}

{{< /highlight >}}
```


توضح هذه الصورة الإخراج بعد تشغيل الكود أعلاه:

![ما يجب القيام به: image_بديل_نص](working-with-user-defined-cells_2.png)
## **قم بإنشاء خلية معرّفة من قبل المستخدم في ورقة الشكل**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) يسمح بإنشاء خلية معرّفة من قبل المستخدم في ورقة الأشكال. يصف هذا المثال الموضوع الطريقة ، يمكن للمطورين إضافة العديد من صفوف User.name كما يحتاجون ، وتعيين أسماء ذات معنى للصفوف ، وتعيين قيم الخلية.
### **إنشاء خلية معرّفة من قبل المستخدم**
يمكن استخدام أسلوب الإضافة الذي تعرضه مجموعة المستخدمين لإنشاء خلية معرّفة من قبل المستخدم في ورقة الأشكال. يأخذ معلمة واحدة.
#### **عينة تكوين خلية البرمجة**
استخدم مثال التعليمات البرمجية التالي في تطبيق .NET الخاص بك لإنشاء خلية معرّفة من قبل المستخدم في ورقة الأشكال باستخدام Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(2);
            
// Initialize user object
User user = new User();
user.Name = "UserDefineCell";
user.Value.Val = "800";
// Add user-defined cell
shape.Users.Add(user);

// Save diagram
diagram.Save(dataDir + "CreateUserDefinedCellInShapeSheet_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **استرجع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال**
Aspose.Diagram for .NET API يسمح باسترداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال. يصف هذا المثال الموضوع الطريقة ، يمكن للمطورين استرداد كل User.name لجميع الأشكال في الرسم.
### **استرداد الخلايا المعرفة من قبل المستخدم**
يمكن استخدام خصائص NameU و Value.Val و Prompt.Value المعروضة بواسطة فئة المستخدم لاسترداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال.
#### **استرجع الخلايا من نماذج برمجة ورقة الأشكال**
استخدم الكود التالي في تطبيق .NET الخاص بك لاسترداد جميع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال باستخدام Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UserDefinedCells();
int count = 0;
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through pages
foreach (Aspose.Diagram.Page objPage in diagram.Pages)
{
    // Iterate through shapes
    foreach (Aspose.Diagram.Shape objShape in objPage.Shapes)
    {
        Console.WriteLine(objShape.NameU);
        // Iterate through user-defined cells
        foreach (Aspose.Diagram.User objUserField in objShape.Users)
        {
            count++;
            Console.WriteLine(count + " - Name: " + objUserField.NameU + " Value: " + objUserField.Value.Val + " Prompt: " + objUserField.Prompt.Value);
        }
    }
}  

{{< /highlight >}}
```
