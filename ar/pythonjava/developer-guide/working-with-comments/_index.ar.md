---
title: التعامل مع التعليقات
type: docs
weight: 210
url: /ar/python-java/working-with-comments/
description: توضح هذه الصفحة كيفية إضافة تعليق على صفحة رسم Visio بمكتبة Aspose.Diagram.
---
## **قم بإضافة تعليق على مستوى الصفحة في Visio**
 Aspose.Diagram لـ Python via Java API يسمح للمطورين بإضافة تعليق في أي مكان على صفحة[الرسم Visio](DrawingComment.vsdx).
### **أضف تعليق**
تسمح لك طريقة addComment ، المكشوفة بواسطة فئة الصفحة ، بإضافة تعليقات إلى صفحة الرسم. يأخذ إحداثيات X و Y جنبًا إلى جنب مع سلسلة تعليق.

Microsoft Visio يقوم المستخدمون باضافة تعليقات للصفحة بأكملها والتي يتم تقديمها بواسطة شارة في الركن الأيسر العلوي من الصفحة. يمكن للمطورين إضافة تعليقات على مستوى الصفحة في Visio. يدعم Aspose.Diagram لـ Python via Java API بالإضافة إلى دعم تعديل التعليق على مستوى الصفحة في Visio.
#### **إضافة نموذج برمجة تعليق على مستوى الصفحة**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("DrawingComment.vsdx")

# Add comment
diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

# Save diagram
diagram.save("AddPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

## **قم بتحرير تعليق على مستوى الصفحة في Visio Diagram**
Aspose.Diagram لـ Python via Java API لديه دعم لتغيير التعليق على مستوى الصفحة على[الرسم Visio](DrawingComment.vsdx) الصفحة التي يتم تقديمها بواسطة رمز في الزاوية العلوية اليسرى من الصفحة.
### **تعديل التعليق**
تسمح الخاصية Comment ، المعروضة بواسطة فئة Annotation ، للمطورين بتحرير التعليقات في صفحة الرسم Visio.
#### **تحرير نموذج برمجة التعليق**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load Visio
diagram = Diagram("DrawingComment.vsdx")

# get collection of the annotations
annotations = diagram.getPages().getPage("Page-1").getPageSheet().getAnnotations()

# iterate through the annotations
for annotation in annotations:
    comment = annotation.getComment().getValue()
    comment += "Updation mark"
    annotation.getComment().setValue(comment)

# save Visio
diagram.save("EditPageLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

## **أضف تعليقًا على مستوى الشكل في رسم Visio**
 Aspose.Diagram لـ Python via Java API يسمح للمطورين بإضافة تعليقات إلى الشكل في[الرسم Visio](DrawingComment.vsdx).
### **أضف تعليق**
تأخذ طريقة addComment المحملة بشكل زائد ، والتي يتم عرضها بواسطة فئة الصفحة ، مثيل فئة الشكل وسلسلة نصية للتعليق.
#### **إضافة نموذج برمجة تعليق على مستوى الشكل**

{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("DrawingComment.vsdx")

# retrieve page by name
page = diagram.getPages().getPage("Page-1")

# retrieve shape by ID
shape = page.getShapes().getShape(1)

page.addComment(shape, "Hello")

# save diagram
diagram.save("AddShapeLevelCommentInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}

