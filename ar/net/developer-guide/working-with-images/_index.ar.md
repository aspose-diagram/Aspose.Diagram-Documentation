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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Load memory stream into bitmap object
            System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);

            // Save bmp here
            bitmap.Save(dataDir + "ExtractAllImages" + shape.ID + "_out.bmp");
        }
    }
}

{{< /highlight >}}
```
## **احصل على أيقونات بأشكال Visio مختلفة**
Aspose.Diagram for .NET API يسمح الآن للمطورين بالحصول على أيقونات بأشكال Visio مختلفة.
### **الحصول على أيقونة الشكل**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram أو استنسل موجود.
1. احصل على إتقان من خلال فهرسها
1. احصل على أيقونة رئيسية.
1. حفظ الرمز في الفضاء المحلي.
#### **احصل على نموذج لبرمجة الأيقونات**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// Get master
Master master = stencil.Masters.GetMaster(1);

using (System.IO.MemoryStream stream = new System.IO.MemoryStream(master.Icon))
{
    // Load memory stream into bitmap object
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(stream);
    // Save as png format
    bitmap.Save(dataDir + "MasterIcon_out.png", System.Drawing.Imaging.ImageFormat.Png);
}

{{< /highlight >}}
```
## **استبدال شكل صورة Visio Diagram**
Aspose.Diagram for .NET API يسمح للمطورين بالوصول إلى أشكال الصور المتاحة واستبدالها في Visio diagram.
### **استبدال شكل صورة**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram موجود.
1. كرر من خلال أشكال الصفحة الانتقائية.
1. قم بتطبيق عامل التصفية للحصول على أشكال الصور.
1. حفظ الناتج Visio diagram في المساحة المحلية.
#### **استبدال نموذج لبرمجة شكل صورة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
// Convert image into bytes array
byte[] imageBytes = File.ReadAllBytes(dataDir + "Picture.png");

// Enter page index i.e. 0 for first one
foreach (Shape shape in diagram.Pages[0].Shapes)
{
    // Filter shapes by type Foreign
    if (shape.Type == Aspose.Diagram.TypeValue.Foreign)
    {
        using (System.IO.MemoryStream stream = new System.IO.MemoryStream(shape.ForeignData.Value))
        {
            // Replace picture shape
            shape.ForeignData.Value = imageBytes;
        }
    }
}

// Save diagram
diagram.Save(dataDir + "ReplaceShapePicture_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **استيراد صورة نقطية كشكل Visio**
Aspose.Diagram for .NET API يسمح الآن للمطورين باستيراد صورة نقطية كشكل Microsoft Visio.
### **أدخل BMP صورة في Visio**
يوضح الرمز الموجود في العينات أدناه كيفية:

1. قم بإنشاء diagram.
1. احصل على Visio صفحة
1. قم باستيراد صورة نقطية كشكل Visio
1. احفظ diagram.
#### **أدخل BMP عينة برمجة صورة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Create a new diagram
Diagram diagram = new Diagram();

// Get page object by index
Page page0 = diagram.Pages[0];
// Set pinX, pinY, width and height
double pinX = 2, pinY = 2, width = 4, hieght = 3;

// Import Bitmap image as Visio shape
page0.AddShape(pinX, pinY, width, hieght, new FileStream(dataDir + "image.bmp", FileMode.OpenOrCreate));

// Save Visio diagram
diagram.Save(dataDir + "InsertImageInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
