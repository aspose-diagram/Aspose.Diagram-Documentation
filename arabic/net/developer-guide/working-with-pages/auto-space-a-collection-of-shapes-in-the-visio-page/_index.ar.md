---
title: تباعد تلقائي لمجموعة من الأشكال في صفحة Visio
type: docs
weight: 30
url: /ar/net/auto-space-a-collection-of-shapes-in-the-visio-page/
description: يشرح هذا القسم كيفية تباعد مجموعة من الأشكال تلقائيًا في صفحة visio مع Aspose.Diagram.
---
## **تباعد تلقائي لمجموعة من الأشكال في صفحة Visio**
باستخدام Aspose.Diagram for .NET API ، يمكن للمطورين وضع مسافة تلقائية لمجموعة من الأشكال في الرسم Visio. من أجل تحقيق ذلك ، تقدم فئة الصفحة عضوًا AutoSpaceShapes الذي يأخذ معلمات ShapeCollection و AutoSpaceOptions. تسمح فئة AutoSpaceOptions بتعيين المسافات الأفقية والعمودية.
### **المسافات التلقائية للأشكال في الصفحة**
استخدم الكود التالي في تطبيق .NET الخاص بك لوضع مسافة تلقائية بين مجموعة من الأشكال في أي صفحة من رسم Visio.

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// get page of the Visio drawing

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.DistanceInHorizontal = 2;

options.DistanceInVertical = 2;

// set auto space 

page.AutoSpaceShapes(page.Shapes, options);

// save Visio drawing

diagram.Save(@"c:\temp\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
