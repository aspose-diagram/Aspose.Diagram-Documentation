---
title: العمل مع الخلايا المعرفة من قبل المستخدم
type: docs
weight: 100
url: /ar/java/working-with-user-defined-cells/
---
## **اقرأ الخلايا المعرفة من قبل المستخدم للأشكال Visio**
 يقوم المستخدمون بإدراج الحقول النصية في الأشكال لعرض معلومات إضافية.**خلايا معرّفة من قبل المستخدم** هو فرع واحد من هذه الحقول ويستخدم هذا الفرع المعلومات التي تم إدخالها في خلية القيمة الخاصة بقسم الخلايا المعرفة من قبل المستخدم في ورقة الشكل الخاصة بالشكل. يمكن للمطورين إدراج وقراءة جميع الخلايا المحددة من قبل المستخدم باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 مجموعة المستخدمين المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) تدعم الفئة كائن com.aspose.diagram.User. ال[المستعمل](https://reference.aspose.com/diagram/java/com.aspose.diagram/User) يمكن استخدام فئة لقراءة الخصائص. هناك عدد قليل من الخلايا المعرفة من قبل المستخدم كما ترى في الصورة التالية:

**جدول يعرض معلومات حول الخلايا المحددة من قبل المستخدم** 

![ما يجب القيام به: image_بديل_نص](working-with-user-defined-cells_1.png)

يتم استخدام الكود التالي لقراءة الخلايا المعرفة من قبل المستخدم.

توضح الصورة التالية الإخراج بعد تشغيل الكود:

![ما يجب القيام به: image_بديل_نص](working-with-user-defined-cells_2.png)
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadUserdefinedCellsOfShape.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(1);
// extract user defined cells of the shape
for (User user :(Iterable<User>) shape.getUsers())
{
    System.out.println(user.getName() + ": " + user.getValue().getVal());
}

{{< /highlight >}}

### **إنشاء خلية معرّفة من قبل المستخدم**
يسمح Aspose.Diagram for Java API للمطورين بإنشاء خلية معرفة بواسطة المستخدم في ورقة الأشكال. يصف هذا المثال الموضوع كيفية إضافة العديد من صفوف اسم المستخدم حسب الحاجة ، وتعيين أسماء ذات معنى للصفوف ، وتعيين قيم الخلية.

يمكن استخدام طريقة الإضافة التي تعرضها مجموعة المستخدمين لإنشاء خلية معرّفة من قبل المستخدم في ورقة الأشكال. يأخذ معلمة واحدة.

استخدم الكود التالي في تطبيق Java الخاص بك لإنشاء خلية معرّفة من قبل المستخدم في ورقة الأشكال باستخدام Aspose.Diagram for Java.
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **استرجع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال**
Aspose.Diagram for Java API يسمح للمطورين باسترداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال. يصف هذا المثال الموضوع كيفية استرداد كافة أسماء المستخدمين لكافة الأشكال في الرسم.
### **استرداد الخلايا المعرفة من قبل المستخدم**
 طرق getNameU () و getValue (). getVal () و getPrompt (). getValue () المكشوفة بواسطة[المستعمل](https://reference.aspose.com/diagram/java/com.aspose.diagram/User)يمكن استخدام class لاسترداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال.
#### **استرجع الخلايا من نماذج برمجة ورقة الأشكال**
استخدم الكود التالي في تطبيق Java الخاص بك لاسترداد جميع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال باستخدام Aspose.Diagram for Java.
#### **عينات البرمجة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateUserDefinedCellInShapeSheet.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(2);
        
// initialize user object
User user = new User();
user.setName("UserDefineCell");
user.getValue().setVal("800");
// add user-defined cell
shape.getUsers().add(user);

// save diagram
diagram.save(dataDir + "CreateUserDefinedCellInShapeSheet_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

