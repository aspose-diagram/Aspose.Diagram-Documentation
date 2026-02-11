---
title: العمل مع عناصر النافذة
type: docs
weight: 130
url: /ar/java/working-with-window-elements/
---
## **استرجع عناصر النافذة من رسم Visio**
 يمكن أن تحتوي نافذة التطبيق Visio الرئيسية على أي ملفات Visio مفتوحة ، مثل متصفحات الويب الحديثة التي تسمح بعدة صفحات ويب مبوبة في نافذة واحدة. يمكن للمطورين استرداد كائنات Window باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

 ال[نافذة جمع](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) يمثل الكائن قائمة[نافذة او شباك](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)الكائنات المتوفرة في الرسم. تدعم خاصية Windows ، المعروضة بواسطة الفئة Diagram ، مجموعة من كائنات Aspose.Diagram.Window. يمكن استخدام هذه الخاصية لاسترداد معلومات النافذة أي معرف النافذة والنوع والارتفاع والعرض والحالة.

**نافذة وحدة التحكم تظهر الإخراج من الكود.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/zduARGh.png)
### **استرجاع نموذج برمجة عناصر النافذة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}
```
## **أضف عنصر النافذة إلى Visio Diagram**
 يمكن أن تحتوي نافذة التطبيق Visio الرئيسية على أي ملفات Visio مفتوحة ، مثل متصفحات الويب الحديثة التي تسمح بعدة صفحات ويب مبوبة في نافذة واحدة. يمكن للمطورين الآن إضافة كائن Window جديد في مثيل Microsoft Visio باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

يمثل عنصر Window نافذة مفتوحة في نسخة Microsoft Visio. تسمح طريقة الإضافة ، المكشوفة بواسطة فئة WindowCollection ، بإضافة كائن Window جديد.
### **إضافة نموذج برمجة عنصر النافذة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **أضف دعمًا للشبكات الديناميكية ونقاط الاتصال**
تساعدك الشبكة الديناميكية على وضع الأشكال الجديدة رأسياً وأفقياً بالنسبة للأشكال التي وضعتها بالفعل في الرسم. فيما يتعلق بنقاط الاتصال ، بمجرد تمييزها على أنها محددة ، ستساعدنا في رؤية نقاط الاتصال عندما نكون في طور الاتصال بها. يمكننا تحقيق كلا الخيارين باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **دعم الشبكات الديناميكية ونقاط الاتصال في رسومات Visio**
تقدم فئة Window خصائص DynamicGridEnabled و ShowConnectionPoints. يمكن استخدام هذه الخصائص لتطبيق الإعدادات لدعم الشبكات الديناميكية وإظهار خيارات نقاط الاتصال.

**تطبيق Visio يعرض الخيارات في Visio.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/bxsJIwF.png)
#### **إضافة نموذج برمجة الدعم**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **إظهار وإخفاء الشبكات والمساطر والأدلة وفواصل الصفحات من Visio Diagram**
 Microsoft Office Visio له زوج من المساطر وشبكة ونوعين من الأدلة وعلم فواصل الصفحات لمعرفة ما سيتم طباعته على كل صفحة. يمكن للمطورين تطبيق هذه الإعدادات باستخدام[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)يتم تطبيق الإعدادات بشكل عام على صفحة واحدة.

تقدم فئة Window خصائص ShowGrid و ShowGuides و ShowRulers و ShowPageBreaks. يمكن استخدام هذه الخصائص لتطبيق الإعدادات لإظهار وإخفاء الشبكات والأدلة والمساطر وفواصل الصفحات.

**تطبيق Visio يعرض الخيارات في Visio.**

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/E0pvXbP.png)
### **عينة البرمجة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
