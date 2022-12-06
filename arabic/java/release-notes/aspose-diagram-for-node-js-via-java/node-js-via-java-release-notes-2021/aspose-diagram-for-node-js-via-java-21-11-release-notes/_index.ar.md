---
title: Aspose.Diagram لـ Node.js via Java 21.11 ملاحظات الإصدار
type: docs
weight: 4
url: /ar/java/aspose-diagram-for-node-js-via-java-21-11-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار لـ Aspose.Diagram لـ Node.js via Java 21.11.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50806|wk: لون InheridetChar|التعزيز|
|DIAGRAMJAVA-50385|يتم تغيير لون الحدود والعناوين عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMJAVA-50501|VSDX إلى PNG - لون الأشكال غير صحيح|حشرة|
|DIAGRAMJAVA-50631|الأشكال غير متناسقة بعد تصدير VSDX إلى PDF|حشرة|
|DIAGRAMJAVA-50804|يتم التفاف نص الموصل عند رسم الموصل|حشرة|
## `?`**عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأية تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه في منتدى الدعم Aspose.Diagram.

### **يضيف PresetTheme في الشكل**
- قم بتطبيق نسق محدد مسبقًا على هذا الشكل.

{{< highlight "java" >}}
 
 shape.setPresetTheme( PresetThemeValue.BUBBLE);

{{< /highlight >}}


### **يضيف PresetThemeVariant في الشكل**
- قم بتطبيق متغير نسق محدد مسبقًا على هذا الشكل

{{< highlight "java" >}}

shape.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);

{{< /highlight >}}

### **يضيف PresetThemeQuickStyle في الشكل**
- قم بتطبيق نمط سريع متغير للنسق مُعد مسبقًا على هذا الشكل

{{< highlight "java" >}}

shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_1);

{{< /highlight >}}
