---
title: Aspose.Diagram for Java 21.2 ملاحظات الإصدار
type: docs
weight: 11
url: /ar/java/aspose-diagram-for-java-21-2-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 21.2.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50710|أضف سطرًا واحدًا إلى ملف Viso ، بحيث يظل قابلاً للتحرير كخط|التعزيز|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **يضيف activePage في Diagram**
- تحدد الصفحة النشطة

{{< highlight "java" >}}

 Page page = diagram.getActivePage()

{{< /highlight >}}
### **يضيف centerDrawing in Shape**
- توسيط الشكل فيما يتعلق بمدى الصفحة

{{< highlight "java" >}}

 shape.centerDrawing()

{{< /highlight >}}
### **يضيف drawLine في الصفحة**
- عملية رسم خط واحد.

{{< highlight "java" >}}

  diagram.getPages().get(0).drawLine(0, 0, 1, 1);

{{< /highlight >}}