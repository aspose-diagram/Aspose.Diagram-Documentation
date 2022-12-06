---
title: Aspose.Diagram for Java 20.2 ملاحظات الإصدار
type: docs
weight: 60
url: /ar/java/aspose-diagram-for-java-20-2-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 20.2.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50361|لا يتم الاحتفاظ بلون مقدمة الشكل عند تحويل VST إلى PNG|التعزيز|
|DIAGRAMJAVA-50504|VSD إلى PDF - تم تغيير لون الخطوط|التعزيز|
## ` `**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **تمت إضافة تكبير الصفحة في ImageSaveOptions**
- يحدد ما إذا كان سيتم تكبير الصفحة أم لا

{{< highlight "java" >}}

 com.aspose.diagram.ImageSaveOptions o = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);

opt.setEnlargePage(false);

{{< /highlight >}}
### **تمت إضافة hasHiddenInfo في Diagram**
- الإشارة إلى ما إذا كان diagram يحتوي على معلومات مخفية

{{< highlight "java" >}}

 diagram.hasHiddenInfo();

{{< /highlight >}}




