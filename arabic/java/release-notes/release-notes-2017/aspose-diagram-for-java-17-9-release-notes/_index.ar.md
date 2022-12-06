---
title: Aspose.Diagram for Java 17.9 ملاحظات الإصدار
type: docs
weight: 40
url: /ar/java/aspose-diagram-for-java-17-9-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.9](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-9-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50485|أضف دعمًا لأشكال التباعد التلقائي في Visio|التعزيز|
|DIAGRAMJAVA-50521|الإخراج VSDX - تخطيط غير صحيح لخط الموصل|حشرة|
|DIAGRAMJAVA-50522|المخرج PNG - يخرج نص الشكل عن الحد|حشرة|
|DIAGRAMJAVA-50527|المخرج VSDX - يلامس خط التوصيل حدود الشكل|حشرة|
|DIAGRAMJAVA-50540|المخرج VSDX - تخطيط غير صحيح للخطوط المتصلة|حشرة|
|DIAGRAMJAVA-50543|الناتج VSDX - تخطيط غير صحيح ونص في غير محله للخطوط المتصلة|حشرة|
|DIAGRAMJAVA-50545|المخرجات VSDX - لا يمكن صياغة موضع النص بالشكل|حشرة|
|DIAGRAMJAVA-50547|الإخراج VSDX - لا يمكن تعيين قيمة الخاصية كسلسلة|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف عضو autoSpaceShapes في الصفحة**
يسمح بإضافة مسافة تلقائية بين مجموعة الأشكال.

{{< highlight "java" >}}

 AutoSpaceOptions options = new AutoSpaceOptions();

diagram.getPages().getPage(0).autoSpaceShapes(diagram.getPages().getPage(0).getShapes(), options);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [تباعد تلقائي لمجموعة من الأشكال في صفحة Visio](/diagram/ar/java/auto-space-a-collection-of-shapes-in-the-visio-page/)
