---
title: Aspose.Diagram لـ Node.js عبر Java 22.11 ملاحظات الإصدار
type: docs
weight: 17
url: /ar/nodejsjava/aspose-diagram-for-node-js-via-java-22-11-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram لـ Node.js عبر Java 22.11.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-51049|كيفية الحصول على نقطة اتصال لخط على شكل|التعزيز|
|DIAGRAMJAVA-51044|.getDisplayText () لفك تشفير كيانات html (Aspose.Diagram Java 22.10، .vsd files)|التعزيز|
|DIAGRAMJAVA-51046|يختلف اسم الشكل أحيانًا عن الأسماء الموجودة في Visio|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف getConnectorRule في الشكل**
- إرجاع قاعدة موصل تحتوي على معرف الشكل والموصل المتصلين بالشكل

{{< highlight "java" >}}
ConnectorRule rule= shape.getConnectorRule();
{{< /highlight >}}

### **يضيف setSavingCustomLinePattern في SVGSaveOptions**
- يحدد ما إذا كان يتم حفظ نمط الخط المخصص.

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions(); 
saveOp.setSavingCustomLinePattern(false);
{{< /highlight >}}
