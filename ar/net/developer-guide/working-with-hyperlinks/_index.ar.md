---
title: العمل مع الارتباطات التشعبية
type: docs
weight: 160
url: /ar/net/working-with-hyperlinks/
description: يشرح هذا القسم كيفية إضافة ارتباط تشعبي أو الحصول عليه في شكل Visio مع Aspose.Diagram.
---
## **أضف ارتباط تشعبي إلى شكل Visio**
Microsoft Office Visio يدعم إضافة الوصلات المرجعية إلى أي شكل. يمكن أن ترتبط الارتباطات التشعبية بصفحة أو شكل آخر في الرسم الحالي ، أو بصفحة أو شكل في رسم آخر ، أو مستند آخر غير رسم Visio ، أو موقع ويب ، أو موقع FTP ، أو عنوان بريد إلكتروني. يمكن للمطورين استخدام Aspose.Diagram API لإضافة ارتباطات تشعبية بسهولة لشكل Visio.

 في الرسم Visio متعدد الصفحات ، يمكن للارتباطات التشعبية أن تنتقل بك من شكل واحد إلى العديد من أنواع الارتباطات الأخرى.[مجموعة الارتباط التشعبي](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يقدم class طريقة Add التي يمكن استخدامها لإضافة ارتباط تشعبي للشكل.

لتحديد العقارات في Microsoft Office Visio:

1. في Visio diagram ، انقر بزر الماوس الأيمن فوق الشكل.
1.  يختار**ارتباط تشعبي.**
1. قم بتعيين الخصائص الموجودة
1.  يضعط**نعم** زر

**بيانات الارتباط التشعبي للشكل ، كما هو موضح في Microsoft Visio**

![ما يجب القيام به: image_بديل_نص](working-with-hyperlinks_1.png)
### **إضافة نموذج برمجة ارتباط تشعبي**
يضيف مقتطف الشفرة أدناه بيانات الارتباط التشعبي للشكل.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **الحصول على بيانات الارتباطات التشعبية لأشكال Visio**
يمكن للمطورين استرداد كافة الارتباطات التشعبية من شكل Visio بنفس طريقة استرجاعها[قراءة بيانات الشكل Visio](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) استخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

في الرسم Visio متعدد الصفحات ، يمكن للارتباطات التشعبية أن تنتقل بك من شكل واحد إلى العديد من أنواع الارتباطات الأخرى.[مجموعة الارتباط التشعبي](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) يتعرض لها[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) فئة تسمح للمطورين باسترداد الارتباطات التشعبية.

لتحديد العقارات في Microsoft Office Visio:

1. في diagram ، انقر بزر الماوس الأيمن فوق شكل.
1.  يختار**ارتباط تشعبي.**

يتم سرد أي خصائص موجودة في مربع الحوار.
**بيانات الارتباط التشعبي للشكل ، كما هو موضح في Microsoft Visio**

![ما يجب القيام به: image_بديل_نص](working-with-hyperlinks_1.png)

**نافذة وحدة تحكم تعرض إخراج بيانات الشكل**

![ما يجب القيام به: image_بديل_نص](working-with-hyperlinks_3.png)
### **احصل على نموذج لبرمجة الارتباطات التشعبية**
يقرأ مقتطف التعليمات البرمجية أدناه بيانات الارتباط التشعبي للشكل.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
