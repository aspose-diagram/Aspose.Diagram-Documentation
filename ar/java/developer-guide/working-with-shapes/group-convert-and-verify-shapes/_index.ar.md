---
title: تجميع وتحويل والتحقق من الأشكال
type: docs
weight: 50
url: /ar/java/group-convert-and-verify-shapes/
---
## **قم بتجميع الأشكال المتعددة معًا في رسم Visio**
Aspose.Diagram API يسمح للمطورين بتجميع الأشكال معًا لنقلها جميعًا مرة واحدة. يحتفظ كل شكل في المجموعة بهوية فريدة وله مجموعة خصائصه الخاصة. عندما نغير تنسيق مجموعة من الأشكال ، فإنه يعين الخاصية الجديدة لكل شكل.
### **كيفية تجميع الأشكال**
يمكن استخدام طريقة المجموعة التي تعرضها فئة ShapeCollection لتجميع الأشكال معًا.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. تهيئة مجموعة من الأشكال
1. الحصول على شكل معين بواسطة معرف.
1. الحصول على شكل معين آخر بواسطة معرف.
1. تعيين الأشكال للمصفوفة.
1. تجميع الأشكال عن طريق استدعاء طريقة المجموعة.
1. احفظ diagram
#### **عينة برمجة الأشكال الجماعية**
استخدم الكود التالي في تطبيق Java لتجميع الأشكال معًا باستخدام Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GroupShapes.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// Initialize an array of shapes
Shape[] ss = new Shape[3];

// extract and assign shapes to the array
ss[0] = page.getShapes().getShape(15);
ss[1] = page.getShapes().getShape(16);
ss[2] = page.getShapes().getShape(17);

// mark array shapes as group
page.getShapes().group(ss);

// save visio diagram
diagram.save(dataDir + "GroupShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **تحويل شكل Visio إلى تنسيقات ملفات أخرى**
Aspose.Diagram for Java API يسمح للمطورين بتحويل شكل Visio واحد إلى أي تنسيق ملف آخر مدعوم. في هذه المقالة ، نقوم بإزالة جميع أشكال Visio الأخرى من الصفحة وتخصيص إعداد الصفحة وفقًا لحجم الشكل المصدر.
### **تحويل شكل Visio معين**
 يمكن للمطورين تحويل شكل Visio إلى PDF و HTML و Image و SVG و SWF بواسطة[تحديد خيارات الحفظ Visio]().
يعمل رمز المثال هذا على النحو التالي:

1. قم بتحميل المصدر Visio.
1. احصل على صفحة معينة.
1. قم بإزالة صفحة الخلفية.
1. قم بإنشاء جدول تجزئة لجميع الأشكال التي تحتوي على المعرفات والأسماء.
1. كرر من خلال جدول التجزئة
1. قم بإزالة كافة الأشكال من صفحة Visio ، باستثناء الشكل المعين.
1. اضبط حجم الصفحة.
1. احفظ الصفحة Visio بأي تنسيق ملف مدعوم.
#### **تحويل نموذج برمجة الشكل**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SaveVisioShapeInOtherFormats.class);   
        
double shapeWidth = 0;
double shapeHeight = 0;

// call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
// get Visio page
Page srcPage = srcVisio.getPages().get(1);
// remove background page
srcPage.setBackPage(null);

// get hash table of shapes, it holds id and name
Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
for (Shape shape : (Iterable<Shape>)srcPage.getShapes())
    // for the normal shape
    remShapes.put(shape.getID(), shape.getName());
        

// iterate through the hash table
Enumeration<Long> enumKey = remShapes.keys();
while(enumKey.hasMoreElements())
{
    Long key = enumKey.nextElement();
    String val = remShapes.get(key);
    Shape shape = srcPage.getShapes().getShape(key);
    // check of the shape name
    if(val.equals("GroupShape1"))
    {
        // move shape to the origin corner
        shapeWidth = shape.getXForm().getWidth().getValue();
        shapeHeight = shape.getXForm().getHeight().getValue();
        shape.moveTo(shapeWidth*0.5, shapeHeight*0.5);
        // trim page size
        srcPage.getPageSheet().getPageProps().getPageWidth().setValue(shapeWidth);
        srcPage.getPageSheet().getPageProps().getPageHeight().setValue(shapeHeight);
    }
    else
    {
        // remove shape from the Visio page and hash table
        srcPage.getShapes().remove(shape);
        remShapes.remove(key);
    }
}

// specify saving options
PdfSaveOptions opts = new PdfSaveOptions();
// set page count to save
opts.setPageCount(1);
// set starting index of the page
opts.setPageIndex(1);
// save it
srcVisio.save(dataDir + "SaveVisioShapeInOtherFormats_Out.pdf", opts);

{{< /highlight >}}
```
### **حوّل Visio إلى PDF**
تسمح طريقة ToPdf لفئة الشكل بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **حوّل Visio إلى HTML**
تسمح طريقة ToHTML لفئة الشكل بتحويل شكل إلى تنسيق HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}} 
## **تحقق مما إذا كان شكلا Visio متصل أو ملتصق**
 Aspose.Diagram for Java API يسمح للمطورين بالتحقق من أن الشكلين Visio ملتصقان أو متصلان. في السابق ، رأينا كيف يمكننا توصيل شكلين أو لصقهما في موضوعات المساعدة هذه:[إضافة وتوصيل Visio الأشكال](/diagram/ar/java/add-and-connect-visio-shapes/) و[أشكال الغراء داخل الحاوية](/diagram/ar/java/working-with-shapes-gluing/).
### **التحقق من الأشكال المتصلة أو الملصقة**
 ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) تقدم الفئة خصائص IsGlued و IsConnected لتحديد ما إذا كان الشكلين ملتصقين أم متصلين.
#### **التحقق من نموذج برمجة الأشكال المتصلة أو الملصقة**
يتحقق الجزء التالي من الكود مما إذا كان الشكلين متصلين أم تم لصقهما.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VerifyConnectedOrGluedShapes.class);  
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// get Visio page by name
Page page = diagram.getPages().getPage("Page-3");

// get Visio shapes by ids
Shape ShapedOne = page.getShapes().getShape(ShapeIdOne);
Shape ShapedTwo = page.getShapes().getShape(ShapeIdTwo);

// determine whether shapes are connected
boolean connected = ShapedOne.isConnected(ShapedTwo);
System.out.println("Shapes are connected: " + connected);

// determine whether shapes are glued
boolean glued = ShapedOne.isGlued(ShapedTwo);
System.out.println("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **تحقق مما إذا كان الشكل Visio في مجموعة من الأشكال**
Aspose.Diagram for Java API يسمح للمطورين بالتحقق من أن الشكل Visio موجود في مجموعة من الأشكال أم لا.
### **التحقق من الشكل في مجموعة الأشكال**
توفر فئة الشكل خصائص IsInGroup لتحديد ما إذا كان الشكل Visio في شكل مجموعة.
#### **التحقق من الشكل في عينة برمجة مجموعة الأشكال**
يتحقق جزء التعليمات البرمجية التالي مما إذا كان الشكل في شكل مجموعة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
				
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
System.out.println("Is it in a Group: " + shape.isInGroup());
{{< /highlight >}}
```

{{% alert color="primary" %}} 

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
