---
title: العمل مع الصور
type: docs
weight: 60
url: /ar/net/working-with-images/
description: يشرح هذا القسم كيفية إدراج أو الحصول على صورة من صفحة visio مع Aspose.Diagram.
---
## **استخراج كافة الصور من صفحة Visio**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. يمكنك استخراج الصور من صفحة معينة لملف Visio.
### **استخراج الصور**
يمثل كائن فئة الصفحة منطقة الرسم لصفحة أمامية أو صفحة خلفية. تدعم خاصية الأشكال المعروضة بواسطة الفئة Diagram مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام هذه الخاصية لاستخراج جميع الصور من صفحة معينة.
#### **عينة برمجة استخراج الصور**
يستخرج الجزء التالي من التعليمات البرمجية جميع الصور من صفحة Visio معينة.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **احصل على أيقونات بأشكال Visio مختلفة**
Aspose.Diagram for .NET API يسمح الآن للمطورين بالحصول على أيقونات بأشكال Visio مختلفة.
### **الحصول على أيقونة الشكل**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram أو استنسل موجود.
1. احصل على إتقان من خلال فهرسها
1. احصل على أيقونة رئيسية.
1. حفظ الرمز في الفضاء المحلي.
#### **احصل على نموذج لبرمجة الأيقونات**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **استبدال شكل صورة Visio Diagram**
Aspose.Diagram for .NET API يسمح للمطورين بالوصول إلى أشكال الصور المتاحة واستبدالها في Visio diagram.
### **استبدال شكل صورة**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram موجود.
1. كرر من خلال أشكال الصفحة الانتقائية.
1. قم بتطبيق عامل التصفية للحصول على أشكال الصور.
1. حفظ الناتج Visio diagram في المساحة المحلية.
#### **استبدال نموذج لبرمجة شكل صورة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **استيراد صورة نقطية كشكل Visio**
Aspose.Diagram for .NET API يسمح الآن للمطورين باستيراد صورة نقطية كشكل Microsoft Visio.
### **أدخل صورة BMP في Visio**
يوضح الرمز الموجود في العينات أدناه كيفية:

1. قم بإنشاء diagram.
1. احصل على Visio صفحة
1. قم باستيراد صورة نقطية كشكل Visio
1. احفظ diagram.
#### **أدخل نموذجًا لبرمجة صورة BMP**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
## **تحويل المساحة المحددة للصفحة Visio إلى صورة**
باستخدام Aspose.Diagram for .NET API ، يمكن للمطورين تحديد منطقة بإحداثيات XY وعرضها وارتفاعها ، ثم تحويل هذه المنطقة إلى تنسيق صورة مدعوم.
### **تحويل Visio منطقة الرسم إلى صورة**
يوضح الرمز الموجود في العينات أدناه كيفية:

1. قم بتحميل رسم Visio موجود
1. تحديد منطقة المستطيل
1. تحويل المنطقة المحددة إلى صورة

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
