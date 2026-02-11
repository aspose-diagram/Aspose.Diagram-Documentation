---
title: العمل مع الطباعة
type: docs
weight: 80
url: /ar/java/working-with-print/
---
## **طباعة Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) يوفر أربع طرق للحمل الزائد لطباعة المخططات. هذه الطرق مرنة بما يكفي لطباعة diagram إلى الطابعة الافتراضية أو إلى أي طابعة متوفرة بإعدادات مخصصة. ما عليك سوى تحديد طريقة الطباعة المناسبة وفقًا للمتطلبات.
### **الطباعة على طابعة معينة**
تتطلب طباعة diagram على الطابعة المحددة اسم الطابعة كمعامل لطريقة الطباعة لـ Diagram. قم بتنفيذ الخطوات التالية لطباعة diagram إلى الطابعة المطلوبة:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- قم باستدعاء أسلوب الطباعة للفئة Diagram باستخدام اسم الطابعة كمعامل سلسلة إلى أسلوب الطباعة
#### **الطباعة على عينة برمجة طابعة معينة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}
```
### **إعداد اسم الطابعة والمستند**
تسمح واجهات برمجة التطبيقات Aspose.Diagram بتعيين اسم الطابعة والوثيقة المحددة لمهمة الطباعة. قم بتنفيذ الخطوات التالية لطباعة diagram على الطابعة المطلوبة:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram الذي سيتم طباعته
- اتصل بأسلوب الطباعة للفئة Diagram باستخدام اسم الطابعة والوثيقة كمعامل سلسلة لأسلوب الطباعة
#### **إعداد نموذج برمجة اسم الطابعة والمستند**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}
```
