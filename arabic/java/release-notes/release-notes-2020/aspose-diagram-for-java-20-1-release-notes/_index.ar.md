---
title: Aspose.Diagram for Java 20.1 ملاحظات الإصدار
type: docs
weight: 70
url: /ar/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 20.1.

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|التعبئة المتدرجة غير مدعومة في التصدير إلى SVG|التعزيز|
|DIAGRAMJAVA-50670|السماح بتحميل الخطوط من الذاكرة|التعزيز|
|DIAGRAMJAVA-50681|API يستغرق وقتًا طويلاً لتحميل diagram ملف بحجم كبير|التعزيز|
|DIAGRAMJAVA-50381|لا يتم الاحتفاظ بأشكال الشبكة عند تحويل VSDX إلى PDF|حشرة|
|DIAGRAMJAVA-50386|تنقلب الصور رأسًا على عقب مع اختلاف اللون عند تحويل VSD إلى SVG|حشرة|
|DIAGRAMJAVA-50679|VSDX إلى PDF - الموصلات مفقودة في الإخراج|حشرة|
|DIAGRAMJAVA-50680|Visio إلى PNG - تم اقتصاص الصور الناتجة|حشرة|
## **عام API والتغييرات غير المتوافقة مع الإصدارات السابقة**
فيما يلي قائمة بأي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram لـ JAVA. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى طرحه على منتدى الدعم Aspose.Diagram.

- تمت إضافة getPages و setPages في الصفحة - يحدد فهرس الصفحات المراد تحميلها.

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- يضيف setFontSources في FontConfigs - يضبط مصادر الخطوط.

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


