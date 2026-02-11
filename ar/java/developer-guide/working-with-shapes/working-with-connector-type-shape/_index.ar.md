---
title: العمل مع شكل نوع الموصل
type: docs
weight: 80
url: /ar/java/working-with-connector-type-shape/
---
## **قم بتعيين مظهر شكل نوع الموصل في Visio**
يوضح هذا الموضوع كيف يمكن للمطورين تغيير مظهر شكل نوع الموصل الديناميكي باستخدام Aspose.Diagram for Java.
### **اضبط مظهر الموصل**
 عرض أسلوب SetConnectorsType بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) يمكن استخدام الفئة لتعيين مظهر شكل نوع الموصل.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل موصل معين.
1. ضبط مظهر الشكل.
1. احفظ diagram
#### **تعيين نموذج برمجة مظهر الموصل**
استخدم الكود التالي في تطبيق Java لتعيين مظهر شكل نوع الموصل باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **حدد خيار إعادة التوجيه لشكل الموصل**
 الخاصية ConFixedCode التي يعرضها ملف[تَخطِيط](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) يمكن استخدام فئة لتحديد خيار إعادة التوجيه. خاصية Layout ، المكشوفة بواسطة ملف[شكل](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) فئة ، سيتم استخدامها.

|<p>**كيفية تحديد خيارات إعادة التوجيه** </p><p>![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الحصول على صفحة معينة.
1. الحصول على شكل موصل معين.
1. تعيين خيارات إعادة التوجيه.
1. احفظ diagram.
### **حدد إعادة توجيه نموذج البرمجة الخيار**
استخدم الكود التالي في تطبيق Java الخاص بك لتحديد خيار إعادة التوجيه لشكل الموصل باستخدام Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

