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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.cs" >}}
## **قم بتحرير تعليق على مستوى الصفحة في Visio Diagram**
 Microsoft Visio يقوم المستخدمون باضافة تعليقات للصفحة بأكملها والتي يتم تقديمها بواسطة شارة في الركن الأيسر العلوي من الصفحة. يمكن للمطورين[إضافة تعليقات على مستوى الصفحة في Visio](/pages/createpage.action?spaceKey=diagramnet&title=Add+a+Page-Level+Comment+in+the+Visio&linkCreation=true&fromPageId=18350768). [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يدعم API بالإضافة إلى ذلك تغيير تعليق مستوى الصفحة في Visio.
### **تعديل التعليق**
 الخاصية Comment ، المكشوفة بواسطة[حاشية. ملاحظة](http://www.aspose.com/api/net/diagram/aspose.diagram/annotation) class ، تسمح للمطورين بتحرير التعليقات في صفحة الرسم Visio.
#### **تحرير نموذج برمجة التعليق**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.cs" >}}
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
