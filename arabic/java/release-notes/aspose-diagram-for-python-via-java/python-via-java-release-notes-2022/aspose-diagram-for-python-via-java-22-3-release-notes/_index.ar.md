---
title: Aspose.Diagram لـ Python عبر Java 22.3 ملاحظات الإصدار
type: docs
weight: 25
url: /ar/java/aspose-diagram-for-python-via-java-22-3-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات ملاحظات الإصدار لـ Aspose.Diagram لـ Python عبر Java 22.3.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50883|تحديد الخطوط المفقودة ومعلومات استبدال الخط من API|حشرة|

## `?`**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف AddText في الصفحة**
- يضيف نص مع تعريف PinX و PinY.

{{< highlight "java" >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}

