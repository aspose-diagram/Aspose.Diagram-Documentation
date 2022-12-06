---
title: Aspose.Diagram for Java 19.3 ملاحظات الإصدار
type: docs
weight: 100
url: /ar/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات إصدار Aspose.Diagram for Java 19.3

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|إضافة دعم لاسترداد دلائل الخطوط الشائعة على أنظمة التشغيل|التعزيز|
|DIAGRAMJAVA-50097|تحويل VSD إلى PDF - تصبح الخطوط المنحنية خطاً مستقيماً|حشرة|
|DIAGRAMJAVA-50161|VTX إلى HTML التحويل - صورة الخلفية لكامل diagram مفقودة|حشرة|
|DIAGRAMJAVA-50301|تصدير VSD إلى PDF - تتحول أشكال نوع Meta إلى رموز فوضوية|حشرة|
|DIAGRAMJAVA-50464|تم عرض الشكل بشكل غير صحيح أثناء تحويل VSDX إلى PNG|حشرة|
|DIAGRAMJAVA-50652|VISIO إلى PDF - يظهر الناتج PDF خطأ في Adobe Reader|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف GetDefaultFontDir في Diagram**
احصل على مسار مجلد الخطوط الافتراضية

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
