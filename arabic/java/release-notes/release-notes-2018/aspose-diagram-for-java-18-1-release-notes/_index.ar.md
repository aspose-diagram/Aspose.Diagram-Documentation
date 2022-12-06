---
title: Aspose.Diagram for Java 18.1 ملاحظات الإصدار
type: docs
weight: 120
url: /ar/java/aspose-diagram-for-java-18-1-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 18.1](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-1-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50200|إضافة دعم لتكرار / استنساخ صفحة diagram|التعزيز|
|DIAGRAMJAVA-50408|حدث خطأ بعد إزالة الصفحة من VSDM|حشرة|
|DIAGRAMJAVA-50577|VDX إلى VSDM - الخطوط المتصلة غير متصلة بشكل صحيح|حشرة|
|DIAGRAMJAVA-50578|VDX إلى VSDM - الخطوط المتصلة غير متصلة بشكل صحيح|حشرة|
|DIAGRAMJAVA-50579|الناتج VDX - وضع جميع أشكال Visio على النقطة المتزامنة|حشرة|
|DIAGRAMJAVA-50580|الناتج VDX - تخطيط غير صحيح للأشكال|حشرة|
### **يضيف نسخ العضو في فئة الصفحة**
يأخذ العضو نسخة نسخة الصفحة الهدف ، كمعامل لاستنساخ هذه الصفحة.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// copy page

newPage.copy(diagram.getPages().get(0));

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [نسخ Visio صفحة إلى نسخة صفحة أخرى]
