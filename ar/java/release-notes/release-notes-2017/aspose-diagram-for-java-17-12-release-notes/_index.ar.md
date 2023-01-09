---
title: Aspose.Diagram for Java 17.12 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/java/aspose-diagram-for-java-17-12-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.12](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-12-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50290|قم بتوفير API المفرد لتحويل شكل Visio إلى PDF|التعزيز|
|DIAGRAMJAVA-50291|قم بتوفير API المفرد لتحويل شكل Visio إلى HTML|التعزيز|
|DIAGRAMJAVA-50572|لا يقوم أسلوب Shape.connectedShapes باسترداد العقد الصادرة|التعزيز|
|DIAGRAMJAVA-50391|يتم إنشاء الصور المعكوسة والأسهم عند تحويل VSD إلى SVG|حشرة|
|DIAGRAMJAVA-50570|VSD إلى PDF - تم إضافة بنود النص الإضافية|حشرة|
|DIAGRAMJAVA-50571|استيراد VSDX - حدث خطأ في عنصر الشكل|حشرة|
|DIAGRAMJAVA-50573|VSD إلى SVG - خطوط شكل المجموعة مفقودة|حشرة|
|DIAGRAMJAVA-50575|VSD إلى SVG - عناصر النص مفقودة|حشرة|
|DIAGRAMJAVA-50576|يؤدي إجراء الاستيراد VDX إلى ظهور خطأ في عنصر الصفحة|حشرة|
### **يضيف نسخ العضو في فئة الشكل**
يأخذ عضو النسخة مثيل الشكل الهدف ، كمعلمة لنسخ هذا الشكل.

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
### **يضيف عضو toPdf في فئة Shape**
يقوم عضو toPdf بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **إضافة عضو toHTML في فئة Shape**
يقوم عضو toHTML بتحويل شكل إلى تنسيق PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [انسخ شكل Visio إلى مثيل Shape آخر](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [حوّل Visio إلى PDF](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-pdf/)
1. [حوّل Visio إلى HTML](https://docs.aspose.com/diagram/java/convert-a-visio-shape-to-html/)


