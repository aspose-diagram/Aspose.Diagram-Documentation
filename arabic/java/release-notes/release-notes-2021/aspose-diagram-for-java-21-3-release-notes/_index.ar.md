---
title: Aspose.Diagram for Java 21.3 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/java/aspose-diagram-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 21.3.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50711|يطرح NullPointerException عند محاولة حفظ مستند VDX كـ PNG|التعزيز|
|DIAGRAMJAVA-50713|مشكلة تداخل النص عند التحويل VSDX إلى PDF|التعزيز|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **تمت إضافة ConnectShapesViaConnector في الصفحة**
- ربط الأشكال via موصل.

{{< highlight "java" >}}

page.connectShapesViaConnector(id, "Port7", id, "Port21", id);

{{< /highlight >}}
### **يضيف GlueShapeToConnectorBeginX في الصفحة**
- شكل الغراء باستخدام BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorBeginX(id, "Port7", id);

{{< /highlight >}}
### **يضيف GlueShapeToConnectorEndX في الصفحة**
- شكل الغراء باستخدام BeginX



{{< highlight "java" >}}

page.glueShapeToConnectorEndX(id, "Port21", id);

{{< /highlight >}}
### **يضيف CenterDrawing في الصفحة**
- توسيط أشكال الصفحة فيما يتعلق بنطاق الصفحة.



{{< highlight "java" >}}

page.centerDrawing();

{{< /highlight >}}
### **يضيف IsContain في الشكل**
- الإشارة إلى ما إذا كان هذا الشكل يحتوي على شكل آخر.



{{< highlight "java" >}}

OLE_Shape.isContain(shape)

{{< /highlight >}}