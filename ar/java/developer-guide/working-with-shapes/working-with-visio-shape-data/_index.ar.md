---
title: العمل مع Visio بيانات الشكل
type: docs
weight: 30
url: /ar/java/working-with-visio-shape-data/
---
## **إضافة شكل جديد في Visio**
Aspose.Diagram for Java يسمح لك بمعالجة Microsoft Visio المخططات بطرق مختلفة. أحد الأشياء التي يمكنك القيام بها هو إضافة أشكال جديدة إلى الرسوم التخطيطية. يتيح لك Aspose.Diagram for Java إضافة شكل جديد إلى diagram. يمكن أيضًا تخصيص الشكل المضاف باستخدام Aspose.Diagram for Java.

يصف هذا الموضوع كيفية إضافة شكل مستطيل جديد إلى diagram.

استخدم Aspose.Diagram for Java's API لإنشاء أشكال جديدة ثم أضف هذه الأشكال إلى مجموعة أشكال diagram.

لإضافة شكل جديد:

1. **ابحث عن الصفحة** - يحتوي كل Visio diagram على مجموعة من الصفحات. يمكن للمطورين استرداد الصفحة حسب معرّف الصفحة أو الاسم وتخزين الصفحة المطلوبة في ملف[صفحة](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)كائن فئة.
1. **أضف المطلوب الرئيسي للشكل** - يحتوي كل Visio diagram على مجموعة من الأساتذة. يمكن للمطورين إضافة رئيسي (بواسطة المعرف أو الاسم) من ملف الاستنسل الموجود (عن طريق المسار المباشر أو دفق الملف).
1. **أضف شكلاً في Visio diagram** - يمكن للمطورين وضع شكل جديد في Visio diagram حسب فهرس الصفحة (يبدأ من 0) ، الاسم الرئيسي ، PinX ، PinY ، الارتفاع (اختياري) والعرض (اختياري).
1. **تعيين خصائص الشكل** - تقوم طريقة AddShape للفئة Diagram بإرجاع معرف الشكل. يمكن للمطورين استرداد الشكل من diagram Visio باستخدام هذا المعرف ، ثم تعيين خصائصه ، مثل اللون والموضع والمحاذاة والنص.

|<p>**المدخلات diagram** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-visio-shape-data_1.png)</p>|<p>**diagram مع إضافة الشكل** </p><p>![ما يجب القيام به: image_بديل_نص](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **إضافة عينة البرمجة**
يوضح مقتطف الشفرة أدناه كيفية القيام بكل خطوة.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **استرجاع معلومات الشكل**
[العمل مع المخططات](/diagram/ar/java/working-with-diagrams/)يشرح كيفية إنشاء الرسوم البيانية وإضافة الأشكال والموصلات ، ثم كيفية استرداد المعلومات حول عناصر diagram مثل[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/), [سادة](/diagram/ar/java/working-with-masters/) والموصلات و[الخطوط](/diagram/ar/java/aspose-diagram-font-operations/). تبحث هذه المقالة في كيفية استرداد معلومات حول الأشكال في diagram.

كل شكل في diagram له معرف واسم. المعرف مهم عند البرمجة باستخدام Visio: إنه الطريقة الرئيسية للوصول إلى الشكل. يحتفظ كل شكل أيضًا بمعلومات حول العنصر الرئيسي (الاستنسل) الذي يتكون منه.

 أ[شكل](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) هو كائن في رسم Visio. تدعم خاصية الأشكال ، المكشوفة بواسطة فئة الصفحة ، مجموعة من Aspose.Diagram كائنات الشكل. يمكن استخدام الخاصية الأشكال لاسترداد معلومات حول الشكل.

في نافذة وحدة التحكم أدناه ، على سبيل المثال ، يمكنك مشاهدة إخراج المعلومات لـ diagram الذي يحتوي على أربعة أشكال: محطتي إنهاء وعملية وموصل ديناميكي. لكل منها معرف فريد بالإضافة إلى اسم الشكل الرئيسي (الاستنسل).

**نافذة وحدة تحكم تعرض معلومات الشكل**

![ما يجب القيام به: image_بديل_نص](working-with-visio-shape-data_3.png)

لاسترداد معلومات الصفحة Visio:

1. يحمل diagram.
1. يقوم بإعداد حلقة foreach للتكرار خلال كل الأشكال الموجودة في diagram.
1. يعرض معلومات الشكل.
### **استرجاع عينة البرمجة**
تسترد قطعة الكود التالية معلومات الشكل من Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 نرحب باستفساراتكم واقتراحاتكم على[Aspose.Diagram المنتدى](https://forum.aspose.com/c/diagram/17). سوف نقوم بالرد على الفور.

{{% /alert %}}
## **انسخ شكل Visio إلى مثيل Shape آخر**
تأخذ طريقة النسخ لفئة الشكل مثيل شكل للنسخ.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **قراءة Visio بيانات الشكل**
 تدعم مجموعة Props المكشوفة بواسطة فئة Shape تنسيق[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) هدف. يمكن استخدام الخاصية لقراءة بيانات الشكل (الخصائص المخصصة).
### **قراءة كافة خصائص الشكل**
لتحديد الخصائص المخصصة في Microsoft Visio:

1. في diagram ، انقر بزر الماوس الأيمن فوق شكل.
1.  يختار**بيانات** ، ومن بعد**بيانات الشكل** من القائمة.
 يتم سرد أي خصائص موجودة في مربع الحوار.

|**بيانات الشكل ، كما هو موضح في Microsoft Visio.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/2loM7b0.png)||


|**نافذة وحدة تحكم تعرض إخراج بيانات الشكل.**|** |
|:- |:- |
|![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/kmAKNrx.png)||
#### **قراءة نموذج البرمجة**
تقرأ مقتطفات التعليمات البرمجية أدناه بيانات الشكل (الخصائص المخصصة).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **اقرأ خاصية الشكل بالاسم**
يقرأ مقتطف الشفرة أدناه خاصية الشكل بالاسم (خاصية مخصصة).
#### **تمت قراءتها حسب نموذج برمجة الاسم**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **استخدم فهارس الاتصال لتوصيل الأشكال**
Aspose.Diagram for Java API يسمح بالفعل للمطورين بإضافة نقاط اتصال جديدة على الشكل ، ويمكن للمطورين الآن توصيل الأشكال باستخدام فهارس الاتصال.
### **استخدم فهارس الاتصال لتوصيل الأشكال**
يمكن استخدام عضو connectShapesViaConnectorIndex المكشوف بواسطة فئة الصفحة لتوصيل الأشكال باستخدام فهارس الاتصال. يوضح الكود التالي كيفية توصيل الأشكال:

1. تهيئة رسم جديد.
1. ضع أربعة أشكال مستطيلة
1. أضف نقطتي اتصال إضافيتين ، بحيث يكون هناك ثلاث نقاط اتصال على خط الحد السفلي
1. قم بتوصيل الشكل الأول من كل اتصال سفلي بأشكال المستطيلات الثلاثة الأخرى من الأعلى باستخدام الموصلات الديناميكية
1. حفظ الرسم
#### **استخدم فهارس الاتصال لتوصيل الأشكال عينة البرمجة**
استخدم الكود التالي في تطبيق Java الخاص بك لتوصيل الأشكال باستخدام فهارس الاتصال مع Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **استرجع الشكل الأصلي لشكل فرعي**
Aspose.Diagram for Java يسمح للمطورين باسترجاع الشكل الرئيسي لشكل فرعي.
### **احصل على شكل الوالدين**
تقدم فئة الشكل خاصية getParentShape لاسترداد الشكل الأصل.
#### **احصل على نموذج برمجة شكل الوالدين**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
