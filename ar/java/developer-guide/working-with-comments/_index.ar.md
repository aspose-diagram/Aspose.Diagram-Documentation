---
title: التعامل مع التعليقات
type: docs
weight: 210
url: /ar/java/working-with-comments/
---
## **قم بإضافة تعليق على مستوى الصفحة في Visio**
Aspose.Diagram for Java API يسمح للمطورين بإضافة تعليق في أي مكان على صفحة الرسم Visio.
### **أضف تعليق**
تسمح لك طريقة addComment ، المكشوفة بواسطة فئة الصفحة ، بإضافة تعليقات إلى صفحة الرسم. يأخذ إحداثيات X و Y جنبًا إلى جنب مع سلسلة تعليق.

 Microsoft Visio يقوم المستخدمون باضافة تعليقات للصفحة بأكملها والتي يتم تقديمها بواسطة شارة في الركن الأيسر العلوي من الصفحة. يمكن للمطورين[إضافة تعليقات على مستوى الصفحة في Visio](). [Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) يدعم API بالإضافة إلى ذلك تغيير تعليق مستوى الصفحة في Visio.
#### **إضافة تعليق عينة البرمجة**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-AddPageLevelCommentInVisio-AddPageLevelCommentInVisio.java" >}}
## **قم بتحرير تعليق على مستوى الصفحة في Visio Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API يدعم تعديل التعليق على مستوى الصفحة في صفحة الرسم Visio والتي يتم تقديمها بواسطة أيقونة في الزاوية اليسرى العليا من الصفحة.
### **تعديل التعليق**
تسمح الخاصية Comment ، المعروضة بواسطة فئة Annotation ، للمطورين بتحرير التعليقات في صفحة الرسم Visio.
#### **تحرير نموذج برمجة التعليق**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Comments-EditPageLevelCommentInVisio-EditPageLevelCommentInVisio.java" >}}
## **أضف تعليقًا على مستوى الشكل في رسم Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API يسمح للمطورين بإضافة تعليقات إلى الشكل في رسم Visio.
### **أضف تعليق**
تأخذ طريقة addComment المحملة بشكل زائد ، والتي يتم عرضها بواسطة فئة الصفحة ، مثيل فئة الشكل وسلسلة نصية للتعليق.
#### **إضافة تعليق عينة البرمجة**
**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
