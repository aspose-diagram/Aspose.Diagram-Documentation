---
title: Aspose.Diagram for Java 18.2 ملاحظات الإصدار
type: docs
weight: 110
url: /ar/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|أضف دعمًا لاسترداد عنصر Char النسبي لجزء النص|التعزيز|
|DIAGRAMJAVA-50478|تمر خطوط الموصل عبر الأشكال الأخرى عند تحويل VDX إلى VSDM|حشرة|
|DIAGRAMJAVA-50581|VSDX إلى PDF - عرض غير صحيح للأشكال|حشرة|
|DIAGRAMJAVA-50582|الخرج VSDX - خطوط التوصيل غير مستقيمة|حشرة|
|DIAGRAMJAVA-50583|استيراد VSD - حدث خطأ في عنصر VisioDocument|حشرة|
|DIAGRAMJAVA-50584|استيراد VDX - حدث خطأ في عنصر VisioDocument|حشرة|
|DIAGRAMJAVA-50585|استيراد VSD - حدث خطأ في عنصر VisioDocument|حشرة|
|DIAGRAMJAVA-50586|VSDX إلى SVG - لون حد غير صحيح للشكل|حشرة|
### **يضيف طريقة getInheritChars في فئة Shape**
يحتوي على قيم الحرف الخاصة بالشكل الذي يرثه الشكل الرئيسي.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
