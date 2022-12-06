---
title: Aspose.Diagram for Java 21.6 ملاحظات الإصدار
type: docs
weight: 7
url: /ar/java/aspose-diagram-for-java-21-6-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 21.6.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50725|تقريب زاوية غير صحيح عند التحويل من vsdx إلى svg|التعزيز|
|DIAGRAMJAVA-50724|الانحدار في Aspose Diagram Java 21.3 - عرض موصل غير صحيح|حشرة|
|DIAGRAMJAVA-50727|Workiva: الحصول على هوامش كتلة النص الافتراضية|حشرة|
|DIAGRAMJAVA-50728|Workiva: تدرج لوني للتعبئة الموروثة|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.
### **يضيف setEmfRenderSetting في SVGSaveOptions**
- الإعداد لعرض ملف تعريف Emf

{{< highlight "java" >}}
SVGSaveOptions saveOp = new SVGSaveOptions();          
saveOp.setEmfRenderSetting(EmfRenderSetting.EMF_PLUS_PREFER);

{{< /highlight >}}
### **يضيف getInheritTextBlock في الشكل**
- يحتوي على قيم كتلة النص للشكل الذي يرثه النمط الأصل والشكل الرئيسي.

{{< highlight "java" >}}

 shape.getInheritTextBlock().getRightMargin().getValue()

{{< /highlight >}}
