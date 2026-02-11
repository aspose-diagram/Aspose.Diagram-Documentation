---
title: التعامل مع التعليقات
type: docs
weight: 220
url: /ar/net/working-with-comments/
description: توضح هذه الصفحة كيفية إضافة التعليقات أو تحريرها باستخدام مكتبة Aspose.Diagram.
---
## **قم بإضافة تعليق على مستوى الصفحة في Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API يسمح للمطورين بوضع التعليقات في أي مكان في Visio صفحة الرسم.
### **أضف تعليق**
 طريقة AddComment ، المكشوفة بواسطة[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class ، تسمح للمطورين بإضافة تعليقات إلى صفحة الرسم. يأخذ إحداثيات X و Y جنبًا إلى جنب مع سلسلة تعليق.
#### **إضافة تعليق عينة البرمجة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add comment
diagram.Pages[0].AddComment(7.205905511811023, 3.880708661417323, "test@");

// Save diagram
diagram.Save(dataDir + "AddComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **قم بتحرير تعليق على مستوى الصفحة في Visio Diagram**
 Microsoft Visio يقوم المستخدمون باضافة تعليقات للصفحة بأكملها والتي يتم تقديمها بواسطة شارة في الركن الأيسر العلوي من الصفحة. يمكن للمطورين[إضافة تعليقات على مستوى الصفحة في Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يدعم API بالإضافة إلى ذلك تغيير تعليق مستوى الصفحة في Visio.
### **تعديل التعليق**
 الخاصية Comment ، المكشوفة بواسطة[حاشية. ملاحظة](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class ، تسمح للمطورين بتحرير التعليقات في صفحة الرسم Visio.
#### **تحرير نموذج برمجة التعليق**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioComments();

// Load Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get collection of the annotations
AnnotationCollection annotations = diagram.Pages.GetPage("Page-1").PageSheet.Annotations;

// Iterate through the annotations
foreach (Annotation annotation in annotations)
{
    string comment = annotation.Comment.Value;
    comment += "Updation mark";
    annotation.Comment.Value = comment;
}
// Save Visio
diagram.Save(dataDir + "EditComment_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **أضف تعليقًا على مستوى الشكل في رسم Visio**
[Aspose.Diagram for .NET](https://www.aspose.com/products/diagram/net)API يسمح للمطورين بإضافة تعليقات إلى الشكل في رسم Visio.
### **أضف تعليق**
طريقة AddComment المحملة بشكل زائد ، والتي يتعرض لها[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)تأخذ class مثيل فئة Shape وسلسلة نصية للتعليق.
#### **إضافة تعليق عينة البرمجة**
**C#**

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
