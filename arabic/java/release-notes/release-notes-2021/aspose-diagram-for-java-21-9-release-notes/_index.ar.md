---
title: Aspose.Diagram for Java 21.9 ملاحظات الإصدار
type: docs
weight: 4
url: /ar/java/aspose-diagram-for-java-21-9-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 21.9.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50753|wk: تحقق من أن TextAnnotation متصل بالشكل|التعزيز|
|DIAGRAMJAVA-50382|تظليل الأشكال مفقود عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMJAVA-50754|wk - LineColor من InheritLine غير صحيح|حشرة|
|DIAGRAMJAVA-50756|wk: PinPos null مقابل مركز الوسط|حشرة|
|DIAGRAMJAVA-50757|WK: قيمة سهم getBegin / End غير صحيحة.|حشرة|
|DIAGRAMJAVA-50771|WK: لا يمكن الحصول على LineColor واسم شكل الورقة|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف الأشكال في الشكل**
- إرجاع مصفوفة تحتوي على معرفات الأشكال التي تعتمد على شكل.



{{< highlight "java" >}}

long[]shapeids = shape.dependsOnShapes();

{{< /highlight >}}
