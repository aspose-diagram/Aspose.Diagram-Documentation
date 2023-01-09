---
title: Aspose.Diagram for Java 18.3 ملاحظات الإصدار
type: docs
weight: 100
url: /ar/java/aspose-diagram-for-java-18-3-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 18.3](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-3-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50592|أضف دعمًا لإرشادات معالجة NewValue|التعزيز|
|DIAGRAMJAVA-50150|لا يمكن الوصول إلى كائنات TabsCollection الخاصة بالشكل|حشرة|
|DIAGRAMJAVA-50588|الناتج VSDX - تم اضافة شكل كبير الحجم|حشرة|
|DIAGRAMJAVA-50593|VSDX إلى SVG - ألوان النص والخلفية غير صحيحة|حشرة|
|DIAGRAMJAVA-50595|Diagram يتحول إلى أبيض وأسود عند حفظ VSDX وثيقة|حشرة|
### **يضيف moveTo عضو في فئة الصفحة**
يأخذ العضو moveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [نقل موضع الصفحة في الرسم Visio]
