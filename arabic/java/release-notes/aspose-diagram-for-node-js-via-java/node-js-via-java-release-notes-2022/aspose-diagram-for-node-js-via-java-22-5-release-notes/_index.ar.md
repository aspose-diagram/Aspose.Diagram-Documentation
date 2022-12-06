---
title: Aspose.Diagram لـ Node.js via Java 22.5 ملاحظات الإصدار
type: docs
weight: 23
url: /ar/java/aspose-diagram-for-node-js-via-java-22-5-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram لـ Node.js via Java 22.5.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50923|wk: القيم المعروضة في الحقل|التعزيز|
|DIAGRAMJAVA-50924|wk: احصل على قيم المحاذاة|التعزيز|
|DIAGRAMJAVA-50934|تحقق من جدوى المعالجة المتوازية لملفات VSDX|حشرة|
|DIAGRAMJAVA-50936|قيم خاطئة لـ Shape.getName () ، Shape.getNameU ()|حشرة|
|DIAGRAMJAVA-50941|تحويل vsd إلى vsdx ، لا يمكن فتح الملف vsdx المحول في Visio.|حشرة|
|DIAGRAMJAVA-50942|تنتهك قيمة "ToSheet" تعريف OpenXML في التحويل من vsd إلى vsdx.|حشرة|
|DIAGRAMJAVA-50943|خطأ أثناء تحميل الملف VSD|حشرة|
|DIAGRAMJAVA-50951|تغيير حجم شكل الخط الجانبي|حشرة|
|DIAGRAMJAVA-50955|ترجع Shape.getXForm (). getWidth () قيمة خاطئة إذا تم تعيين العرض لاستخدام الصيغة|حشرة|

## `?`**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف getDisplayValue في الحقل**
- الحصول على قيمة السلسلة المنسقة لهذا الحقل.

{{< highlight "java" >}}
String str = shape.getFields().get(0).getDisplayValue();
System.out.println(str);
{{< /highlight >}}

### **يضيف getInheritParas في الشكل**
- يحتوي على الفقرات الخاصة بالشكل الذي يرثه النمط الأصل والشكل الرئيسي

{{< highlight "java" >}}
int str = shape.getInheritParas().get(0).getHorzAlign().getValue();
System.out.println(str);
{{< /highlight >}}
