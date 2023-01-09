---
title: Aspose.Diagram لـ Python via Java 22.6 ملاحظات الإصدار
type: docs
weight: 22
url: /ar/java/aspose-diagram-for-python-via-java-22-6-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات ملاحظات الإصدار لـ Aspose.Diagram لـ Python via Java 22.6.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50963|WK: الشكل مشوه بعد الحفظ في PNG|التعزيز|
|DIAGRAMJAVA-50967|تغيير حجم شكل الخط الجانبي [تابع]|حشرة|
|DIAGRAMJAVA-50972|API لا يتم تحليل الملف بشكل صحيح|حشرة|
|DIAGRAMJAVA-50974|مشكلة في إضافة نقطة اتصال جديدة|حشرة|

## `?`**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف الدقة في HTMLSaveOptions**
- الحصول على دقة وضوح HTML التي تم إنشاؤها أو تعيينها ، بالنقاط في البوصة

{{< highlight "java" >}}
HTMLSaveOptions option = new HTMLSaveOptions();
option.setResolution(96);
{{< /highlight >}}
