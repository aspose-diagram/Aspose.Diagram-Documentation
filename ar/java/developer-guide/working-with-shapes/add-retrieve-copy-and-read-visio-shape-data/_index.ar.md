---
title: إضافة بيانات الشكل واستردادها ونسخها وقراءتها Visio
type: docs
weight: 10
url: /ar/java/add-retrieve-copy-and-read-visio-shape-data/
description: يشرح هذا القسم كيفية إضافة شكل أو تعيين خاصية الشكل أو نسخ شكل باستخدام Aspose.Diagram.
---
## **إضافة شكل جديد في Visio**
Aspose.Diagram for Java يسمح لك بمعالجة Microsoft Visio المخططات بطرق مختلفة. أحد الأشياء التي يمكنك القيام بها هو إضافة أشكال جديدة إلى الرسوم التخطيطية. يتيح لك Aspose.Diagram for Java إضافة شكل جديد إلى diagram. يمكن أيضًا تخصيص الشكل المضاف باستخدام Aspose.Diagram for Java.

يصف هذا الموضوع كيفية إضافة شكل مستطيل جديد إلى diagram.

استخدم Aspose.Diagram for Java API لإنشاء أشكال جديدة ثم قم بإضافة هذه الأشكال إلى مجموعة أشكال diagram.

لإضافة شكل جديد:

1. **ابحث عن الصفحة** - يحتوي كل Visio diagram على مجموعة من الصفحات. يمكن للمطورين استرداد الصفحة حسب معرّف الصفحة أو الاسم وتخزين الصفحة المطلوبة في ملف[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)كائن فئة.
1. **أضف المطلوب الرئيسي للشكل** - يحتوي كل Visio diagram على مجموعة من الأساتذة. يمكن للمطورين إضافة رئيسي (بواسطة المعرف أو الاسم) من ملف الاستنسل الموجود (عن طريق المسار المباشر أو دفق الملف).
1. **أضف شكلاً في Visio diagram** - يمكن للمطورين وضع شكل جديد في Visio diagram حسب فهرس الصفحة (يبدأ من 0) ، الاسم الرئيسي ، PinX ، PinY ، الارتفاع (اختياري) والعرض (اختياري).
1. **تعيين خصائص الشكل** - تقوم طريقة AddShape للفئة Diagram بإرجاع معرف الشكل. يمكن للمطورين استرداد الشكل من diagram Visio باستخدام هذا المعرف ، ثم تعيين خصائصه ، مثل اللون والموضع والمحاذاة والنص.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**diagram مع إضافة الشكل** </p><p>![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **إضافة عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية القيام بكل خطوة.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddingNewShape.class);  
//Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-2");

// Add master with stencil file path and master id
String masterName = "Rectangle";
// Add master with stencil file path and master name
diagram.addMaster(dataDir + "Basic Shapes.vss", masterName);
            
// page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
//Add a new rectangle shape
long rectangleId = diagram.addShape(pinX, pinY, width, height, masterName, PageIndex);
            
// set shape properties 
Shape rectangle = page.getShapes().getShape(rectangleId);
rectangle.getXForm().getPinX().setValue(5);
rectangle.getXForm().getPinY().setValue(5);
rectangle.setType(TypeValue.SHAPE);
rectangle.getText().getValue().add(new Txt("Aspose Diagram"));
rectangle.setTextStyle(diagram.getStyleSheets().get(3));
rectangle.getLine().getLineColor().setValue("#ff0000");
rectangle.getLine().getLineWeight().setValue(0.03);
rectangle.getLine().getRounding().setValue(0.1);
rectangle.getFill().getFillBkgnd().setValue("#ff00ff");
rectangle.getFill().getFillForegnd().setValue("#ebf8df");

diagram.save(dataDir + "AddShape_Out.vsdx", SaveFileFormat.VSDX);
System.out.println("Shape has been added.");

{{< /highlight >}}
```

{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **استرجاع معلومات الشكل**
[العمل مع المخططات](/diagram/ar/java/working-with-diagrams/)يشرح كيفية إنشاء الرسوم البيانية وإضافة الأشكال والموصلات ، ثم كيفية استرداد المعلومات حول عناصر diagram مثل[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/), [سادة](https://docs.aspose.com/diagram/java/working-with-masters/), [موصلات](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection) و[الخطوط](https://reference.aspose.com/diagram/java/com.aspose.diagram/FontCollection). تبحث هذه المقالة في كيفية استرداد معلومات حول الأشكال في diagram.

كل شكل في diagram له معرف واسم. المعرف مهم عند البرمجة باستخدام Visio: إنه الطريقة الرئيسية للوصول إلى الشكل. يحتفظ كل شكل أيضًا بمعلومات حول العنصر الرئيسي (الاستنسل) الذي يتكون منه.

 أ[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) هو كائن في رسم Visio. تدعم خاصية الأشكال ، المكشوفة بواسطة فئة الصفحة ، مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام الخاصية الأشكال لاسترداد معلومات حول الشكل.

في نافذة وحدة التحكم أدناه ، على سبيل المثال ، يمكنك مشاهدة إخراج المعلومات لـ diagram الذي يحتوي على أربعة أشكال: محطتي إنهاء وعملية وموصل ديناميكي. لكل منها معرف فريد بالإضافة إلى اسم الشكل الرئيسي (الاستنسل).

|**نافذة وحدة تحكم تعرض معلومات الشكل**|
|:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_3.png)|
لاسترداد معلومات الصفحة Visio:

1. يحمل diagram.
1. يقوم بإعداد حلقة foreach للتكرار خلال كل الأشكال الموجودة في diagram.
1. يعرض معلومات الشكل.
### **استرجاع عينة البرمجة**
تسترد قطعة الكود التالية معلومات الشكل من Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveShapeInfo.class);

//Load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveShapeInfo.vsd");

for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().getPage(0).getShapes())
{
    //Display information about the shapes
    System.out.println("\nShape ID : " + shape.getID());
    System.out.println("Name : " + shape.getName());
    System.out.println("Master Shape : " + shape.getMaster().getName());
}

{{< /highlight >}}
```

## **نسخ الأشكال من Visio موجود**
Aspose.Diagram for Java API يسمح للمطورين بنسخ الأشكال من صفحة المصدر Visio إلى صفحة Visio diagram الجديدة. كما يدعم نسخ أشكال المجموعة. توضح هذه المقالة كيفية نسخ كافة الأشكال من الصفحة diagram المصدر.

لنسخ الأشكال ، يجب على المطورين أيضًا نسخ نسق ورقة الصفحة والمصدر Visio المصدر للاحتفاظ بنمط تعبئة الشكل وخصائص التنسيق الأخرى.

هذا المثال يعمل على النحو التالي:

1. قم بتحميل المصدر Visio.
1. تهيئة Visio جديد
1. قم بإضافة الأساسيات والنُسق من المصدر Visio.
1. احصل على الصفحة من المصدر Visio.
1. انسخ ورقة الصفحة الخاصة بها إلى صفحة Visio الجديدة.
1. التكرار من خلال أشكال الصفحة Visio المصدر.
1. قم بتعيين معرفه الجديد وأضفه إلى صفحة Visio الجديدة.
1. احفظ Visio الجديد في التخزين المحلي.
### **عينة برمجة نسخ**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyShape.class); 
// load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
        
// initialize a new Visio
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.getMasters();
for (Master master : (Iterable<Master>) originalMasters)
    newDiagram.addMaster(srcVisio, master.getName());

// get the page object from the original diagram
Page SrcPage = srcVisio.getPages().getPage("Page-1");
// copy themes from the source diagram
newDiagram.copyTheme(srcVisio);
// copy pagesheet of the source Visio page
newDiagram.getPages().get(0).getPageSheet().copy(SrcPage.getPageSheet());

// copy shapes from the source Visio page
for (Shape shape :(Iterable<Shape>) SrcPage.getShapes())
{
    newDiagram.getPages().get(0).getShapes().add(shape);
}
// save the new Visio
newDiagram.save(dataDir + "CopyShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```


{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **انسخ شكل Visio إلى مثيل Shape آخر**
تأخذ طريقة النسخ الخاصة بفئة الشكل مثيل شكل للنسخ.

## **قراءة Visio بيانات الشكل**
 مجموعة Props التي كشفها[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) فئة تدعم[Aspose.Diagram.Prop](http://www.aspose.com/api/java/diagram/com.aspose.diagram/prop) هدف. يمكن استخدام الخاصية لقراءة بيانات الشكل (الخصائص المخصصة).
### **قراءة كافة خصائص الشكل**
لتحديد الخصائص المخصصة في Microsoft Visio:

1. في diagram ، انقر بزر الماوس الأيمن فوق شكل.
1.  يختار**بيانات** ، ومن بعد**بيانات الشكل** من القائمة.
 يتم سرد أي خصائص موجودة في مربع الحوار.

|**بيانات الشكل ، كما هو موضح في Microsoft Visio.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**نافذة وحدة تحكم تعرض إخراج بيانات الشكل.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **قراءة نموذج البرمجة**
تقرأ مقتطفات التعليمات البرمجية أدناه بيانات الشكل (الخصائص المخصصة).

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadAllShapeProps.class);  

// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        for (Prop property :(Iterable<Prop>) shape.getProps())
        {
            System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
        }
        break;
    }
}

{{< /highlight >}}
```

### **اقرأ خاصية الشكل بالاسم**
يقرأ مقتطف الشفرة أدناه خاصية الشكل بالاسم (خاصية مخصصة).
#### **تمت قراءتها حسب نموذج برمجة الاسم**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadShapePropByName.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process1")
    {
        Prop property = shape.getProps().getProp("Name1");
        System.out.println(property.getLabel().getValue() + ": " + property.getValue().getVal());
    }
}

{{< /highlight >}}
```

## **استخدم فهارس الاتصال لتوصيل الأشكال**
Aspose.Diagram for Java API يسمح بالفعل للمطورين بإضافة نقاط اتصال جديدة على الشكل ، ويمكن للمطورين الآن توصيل الأشكال باستخدام فهارس الاتصال.
### **استخدم فهارس الاتصال لتوصيل الأشكال**
يتم عرض عضو ConnectShapesViaConnectorIndex بواسطة ملف[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)يمكن استخدام class لتوصيل الأشكال باستخدام فهارس الاتصال.

1. تهيئة رسم جديد.
1. ضع أربعة أشكال مستطيلة
1. أضف نقطتي اتصال إضافيتين ، بحيث يكون هناك ثلاث نقاط اتصال على خط الحد السفلي
1. قم بتوصيل الشكل الأول من كل اتصال سفلي بأشكال المستطيلات الثلاثة الأخرى من الأعلى باستخدام الموصلات الديناميكية
1. حفظ الرسم
#### **استخدم فهارس الاتصال لتوصيل الأشكال عينة البرمجة**
استخدم الكود التالي في تطبيق Java الخاص بك لتوصيل الأشكال باستخدام فهارس الاتصال مع Aspose.Diagram for Java API.

## **استرجع الشكل الأصلي لشكل فرعي**
Aspose.Diagram for Java يسمح للمطورين باسترجاع الشكل الرئيسي لشكل فرعي.
### **احصل على شكل الوالدين**
ال[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape)تقدم الفئة خاصية ParentShape لاسترداد الشكل الأصل.
#### **احصل على نموذج برمجة شكل الوالدين**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveTheParentShape.class) + "Shapes\\";
		
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(13).getShapes().getShape(2);
Shape parentShape = shape.getParentShape();
System.out.println("Parent Shape's Properties:");
System.out.println("Shape ID: " + parentShape.getID());
System.out.println("Shape Name: " + parentShape.getName());
System.out.println("Shape Type: " + parentShape.getType());
{{< /highlight >}}
```

