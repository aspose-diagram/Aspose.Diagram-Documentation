---
title: Aspose.Diagram لـ Python via Java 22.10 ملاحظات الإصدار
type: docs
weight: 18
url: /ar/python-java/aspose-diagram-for-python-via-java-22-10-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات ملاحظات الإصدار لـ Aspose.Diagram لـ Python via Java 22.10.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-51028|setTopPage لا يعمل|التعزيز|
|DIAGRAMJAVA-51035|wk: لم يتم حل خاصية Geoms لبعض أشكال الأوراق بشكل صحيح|التعزيز|
|DIAGRAMJAVA-51030|أحيانًا يختلف .getName () عن الأسماء الموجودة في Visio (Aspose.Diagram Java 22.9 ، .vsd ملفات)|حشرة|
|DIAGRAMJAVA-51033|أحيانًا يختلف .getText () عن الشكل. النص الموجود في Visio (Aspose.Diagram Java 22.9، .vsd)|حشرة|
|DIAGRAMJAVA-51038|عندما يحتوي النص على فواصل أسطر ، فإن إعادة حساب عرض النص غير صحيحة|حشرة|
|DIAGRAMJAVA-51040|.getNameU () فارغة أحيانًا (Aspose.Diagram Java 22.9 ، .vsd ملفات)|حشرة|

## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف getDisplayText في الشكل**
- احصل على النص المعروض على الواجهة

{{< highlight "java" >}}
string text = shape.getDisplayText();
{{< /highlight >}}

### **يضيف getInheritGeoms في الشكل**
- يحتوي على قيم Geoms للشكل الذي يرثه الشكل الرئيسي.

{{< highlight "java" >}}
int count = shape.getInheritGeoms().get(0).getCoordinateCol().getCount();
{{< /highlight >}}