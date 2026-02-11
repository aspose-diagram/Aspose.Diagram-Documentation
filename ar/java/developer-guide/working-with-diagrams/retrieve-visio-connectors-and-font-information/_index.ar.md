---
title: استرجع Visio الموصلات ومعلومات الخط
type: docs
weight: 20
url: /ar/java/retrieve-visio-connectors-and-font-information/
---
## **استرداد معلومات الموصل**
 يوفر Aspose.Diagram for Java آليات لاسترجاع المعلومات - المعرف والاسم - حول[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/) و[رئيسي - سيد](). كما يتيح لك الحصول على معلومات حول الموصلات والعناصر التي تربط الأشكال.

 ال[الاتصال](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) يمثل الكائن الموصل الذي يربط شكلين على Visio صفحة رسم. الخاصية Connects ، المكشوفة بواسطة[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) فئة تدعم مجموعة من Aspose.Diagram.Connect الكائنات. يمكن استخدام هذه الخاصية لاسترداد معلومات المعرف والاسم حول الموصل.

**تظهر نافذة وحدة التحكم الإخراج من الكود أدناه.** 

![ما يجب القيام به: image_بديل_نص](retrieve-visio-connectors-and-font-information_1.png)
### **عينة البرمجة**
يسترد جزء الكود التالي المعلومات الخاصة بالموصلات في diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveConnectorInfo.class);
        
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");        
for(Connect connector : (Iterable<Connect>) diagram.getPages().getPage(0).getConnects())
{
    // Display information about the Connectors
    System.out.println("\nFrom Shape ID : " + connector.getFromSheet());
    System.out.println("To Shape ID : " + connector.getToSheet());
 }

System.out.println("Process Completed Successfully");

{{< /highlight >}}
```
## **استرداد معلومات الخط**
 Aspose.Diagram لديه آليات لاسترجاع المعلومات حول العناصر التي تشكل diagram ، من[الصفحات](/diagram/ar/java/retrieve-get-copy-and-insert-a-page/), [الإستنسل](), [موصلات](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)وكذلك الخطوط. يوضح هذا المقال كيفية معرفة الخطوط المستخدمة في diagram.

 ال[الخط](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) يمثل الكائن محرفًا يتم تطبيقه على نص في مستند أو متاح للاستخدام على النظام.

يقوم كائن الخط بتعيين اسم (على سبيل المثال ، "Arial") لمعرف الخط (على سبيل المثال ، 3) الذي يخزنه Microsoft Visio في خلية خط في قسم حرف لشكل يحتوي على نص منسق باستخدام هذا الخط. يمكن أن تتغير معرفات الخطوط عند فتح مستند على أنظمة مختلفة أو عند تثبيت الخطوط أو إزالتها.
### **استرجاع نموذج برمجة الخط**
يسترد جزء الكود التالي معلومات الخط من Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveFontInfo.class);

// call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveFontInfo.vsd");

for(Font font : (Iterable<Font>) diagram.getFonts())
{
    // Display information about the fonts
    System.out.println(font.getName());
}

System.out.println("Process Completed Successfully");

{{< /highlight >}}
```

![ما يجب القيام به: image_بديل_نص](retrieve-visio-connectors-and-font-information_2.png)
### **الحصول على دليل الخطوط الافتراضي**
Aspose.Diagram for Java API يسمح أيضًا بالحصول على مسار دليل الخط الافتراضي باستخدام طريقة getDefaultFontDir () من Diagram Class. يسترد جزء الكود التالي دليل الخط الافتراضي من Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}
```
