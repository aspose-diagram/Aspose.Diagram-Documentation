---
title: تباعد تلقائي لمجموعة من الأشكال في صفحة Visio
type: docs
weight: 30
url: /ar/java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **تباعد تلقائي لمجموعة من الأشكال في صفحة Visio**
باستخدام Aspose.Diagram for Java API ، يمكن للمطورين وضع مسافة تلقائية لمجموعة من الأشكال في الرسم Visio. من أجل تحقيق ذلك ، تقدم فئة الصفحة عضوًا autoSpaceShapes الذي يأخذ معلمات ShapeCollection و AutoSpaceOptions. تسمح فئة AutoSpaceOptions بتعيين المسافات الأفقية والعمودية.
### **المسافات التلقائية للأشكال في الصفحة**
استخدم الكود التالي في تطبيق Java الخاص بك لوضع مسافة تلقائية بين مجموعة من الأشكال في أي صفحة من رسم Visio.

**Java**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page of the Visio drawing

Page page = diagram.getPages().getPage("Page-1");

// initialize auto space options

AutoSpaceOptions options = new AutoSpaceOptions();

// set horizontal and vertical distances

options.setDistanceInHorizontal(2);

options.setDistanceInVertical(2);

// set auto space 

page.autoSpaceShapes(page.getShapes(), options);

// save Visio drawing

diagram.save("c:\\temp\\AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
