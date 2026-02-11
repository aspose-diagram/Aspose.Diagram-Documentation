---
title: العمل مع الصور
type: docs
weight: 70
url: /ar/java/working-with-images/
---
## **استخراج كافة الصور من صفحة Visio**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. يمكنك استخراج الصور من صفحة معينة لملف Visio.
### **استخراج الصور**
يمثل كائن فئة الصفحة منطقة الرسم لصفحة أمامية أو صفحة خلفية. تدعم خاصية الأشكال المعروضة بواسطة الفئة Diagram مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام هذه الخاصية لاستخراج جميع الصور من صفحة معينة.
#### **عينة برمجة استخراج الصور**
يستخرج الجزء التالي من التعليمات البرمجية جميع الصور من صفحة Visio معينة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
## **احصل على أيقونات بأشكال Visio مختلفة**
Aspose.Diagram for Java API يسمح الآن للمطورين بالحصول على أيقونات بأشكال Visio مختلفة.
### **الحصول على أيقونة الشكل**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram أو استنسل موجود.
1. احصل على إتقان من خلال فهرسها
1. احصل على أيقونة رئيسية.
1. حفظ الرمز في الفضاء المحلي.
#### **احصل على نموذج لبرمجة الأيقونات**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetShapeIcon.class);  
// Load stencil file to a diagram object
Diagram stencil = new Diagram(dataDir + "Timeline.vss");
// get master
Master master = stencil.getMasters().getMasterByName("Triangle");
// get byte array
byte[] bytes = master.getIcon();
// create an image file
FileOutputStream fos = new FileOutputStream(dataDir + "MasterIcon_Out.png");
// write byte array of the image
fos.write(bytes);
// close array
fos.close();

{{< /highlight >}}
```
## **استبدال شكل صورة Visio Diagram**
Aspose.Diagram for Java API يسمح للمطورين بالوصول إلى أشكال الصور المتاحة واستبدالها في Visio diagram.
### **استبدال شكل صورة**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بتحميل diagram موجود.
1. كرر من خلال أشكال الصفحة الانتقائية.
1. قم بتطبيق عامل التصفية للحصول على أشكال الصور.
1. حفظ الناتج Visio diagram في المساحة المحلية.
#### **استبدال نموذج لبرمجة شكل صورة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReplaceShapePicture.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");
        
// convert image into bytes array       
File fi = new File(dataDir + "Picture.png");
byte[] fileContent = Files.readAllBytes(fi.toPath());
		
// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        //replace picture shape
    	shape.getForeignData().setValue(fileContent);
    }
}

// save diagram
diagram.save(dataDir + "ReplaceShapePicture_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **استيراد صورة نقطية كشكل Visio**
Aspose.Diagram for Java API يسمح الآن للمطورين باستيراد صورة نقطية كشكل Microsoft Visio.
### **أدخل BMP صورة في Visio**
يوضح الكود الموجود في العينات أدناه كيفية:

1. قم بإنشاء diagram.
1. احصل على Visio صفحة
1. قم باستيراد صورة نقطية كشكل Visio
1. احفظ diagram.
#### **أدخل BMP عينة برمجة صورة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExtractAllImagesFromPage.class);
// call a Diagram class constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExtractAllImagesFromPage.vsd");

// Enter page index i.e. 0 for first one
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    // Filter shapes by type Foreign
    if (shape.getType() == TypeValue.FOREIGN)
    {
        FileOutputStream fos = new FileOutputStream(dataDir+ "ExtractAllImages" + shape.getID() + "_Out.bmp");
        fos.write(shape.getForeignData().getValue());
        fos.close();
    }
}

{{< /highlight >}}
```
