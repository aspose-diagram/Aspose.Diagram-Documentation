---
title: Aspose.Diagram لـ Node.js عبر Java 21.12 ملاحظات الإصدار
type: docs
weight: 3
url: /ar/java/aspose-diagram-for-node-js-via-java-21-12-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram لـ Node.js عبر Java 21.12.


{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50838|توسيط النص على موصل خط مستقيم|حشرة|
|DIAGRAMJAVA-50839|تحتاج إلى رسم موصل مستقيم بين الأشكال|حشرة|
## `?`**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.


### **يضيف IsSavingImageSeparately في SVGSaveOptions**
- يحدد ما إذا كان يتم حفظ الصورة بشكل منفصل.

{{< highlight "java" >}}

    SVGSaveOptions o = new SVGSaveOptions();
    o.setIsSavingImageSeparately(true);

{{< /highlight >}}


### **يضيف CustomImagePath في SVGSaveOptions**
- المسار المخصص للمستخدم (URL) المحفوظ في ملف svg الذي تم إنشاؤه للصورة. إذا لم يتم تحديده من قبل المستخدم ، فسيتم استخدام الدليل الحالي.

{{< highlight "java" >}}

  o.setCustomImagePath("d:/output/");

{{< /highlight >}}

### **يضيف SaveForegroundPagesOnly في PrintSaveOptions**
- يحدد ما إذا كانت جميع الصفحات ستتم طباعتها أم في المقدمة فقط.

{{< highlight "java" >}}

 options.setSaveForegroundPagesOnly(true);

{{< /highlight >}}
