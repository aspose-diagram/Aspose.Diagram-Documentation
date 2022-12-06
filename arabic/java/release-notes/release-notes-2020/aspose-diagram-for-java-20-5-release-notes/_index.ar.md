---
title: Aspose.Diagram for Java 20.5 ملاحظات الإصدار
type: docs
weight: 30
url: /ar/java/aspose-diagram-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 20.5.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50487|تم إزاحة عناصر النص عند تحويل VSD إلى SVG|التعزيز|
|DIAGRAMJAVA-50692|تم وضع النص الغامق بشكل غير صحيح عند حفظ VSDX كـ SVG|التعزيز|
|DIAGRAMJAVA-50693|الصور غير موجودة في الناتج SVG|حشرة|
|DIAGRAMJAVA-50695|لا يمكن حفظ الملف VSDX كصورة - فإنه يطرح NullPointerException|حشرة|
## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram لـ JAVA. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى طرحه على منتدى الدعم Aspose.Diagram.
### **يضيف متداخل في الشكل**
يشير إلى ما إذا كان هذا الشكل يتقاطع مع شكل آخر.

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
