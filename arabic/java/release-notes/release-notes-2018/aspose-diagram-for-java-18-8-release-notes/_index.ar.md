---
title: Aspose.Diagram for Java 18.8 ملاحظات الإصدار
type: docs
weight: 50
url: /ar/java/aspose-diagram-for-java-18-8-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 18.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-8-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50611|دعم إعداد الإعدادات المحلية باستخدام API|التعزيز|
|DIAGRAMJAVA-50606|VSDX إلى SVG - عرض غير صحيح للأسهم|حشرة|
|DIAGRAMJAVA-50610|موقع النص على الموصلات خاطئ في ملف الإخراج VSDX|حشرة|
|DIAGRAMJAVA-50612|تعذر فتح ملف الإخراج VDX باستخدام Visio Viewer 2010 Professional|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفون أو المهملون بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعها في ال[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
#### **تمت إضافة setLocale في LoadOption**
{{< highlight "java" >}}

         LoadOptions loadOptions = new LoadOptions( LoadFileFormat.VDX ); 

        loadOptions.setLocale(Locale.US);

        Diagram diagram = new Diagram("test.vdx", loadOptions); 

{{< /highlight >}}

يحدد الإعدادات المحلية المستخدمة في diagram وقت تحميل الملف.
