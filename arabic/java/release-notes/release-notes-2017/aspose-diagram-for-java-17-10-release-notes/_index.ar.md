---
title: Aspose.Diagram for Java 17.10 ملاحظات الإصدار
type: docs
weight: 30
url: /ar/java/aspose-diagram-for-java-17-10-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.10](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-10-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50560|لا يكون لـ JpegQuality أي تأثير على مستند الإخراج|التعزيز|
|DIAGRAMJAVA-50548|المخرج VSDX - الخط الواصل الذي يمر عبر حدود الشكل|حشرة|
|DIAGRAMJAVA-50550|لا يحتفظ قسم تحويل الشكل بالصيغ|حشرة|
|DIAGRAMJAVA-50551|VSDX إلى PNG - عرض غير صحيح لزوايا الشكل|حشرة|
|DIAGRAMJAVA-50552|لا يتم الاحتفاظ بألوان التعبئة عند حفظ رسم Visio إلى SVG|حشرة|
|DIAGRAMJAVA-50553|عرض غير صحيح للخطوط عند حفظ رسم Visio إلى SVG|حشرة|
|DIAGRAMJAVA-50554|لا يتم الاحتفاظ بألوان التعبئة عند حفظ رسم Visio إلى SVG|حشرة|
|DIAGRAMJAVA-50555|عرض غير صحيح للخطوط عند حفظ رسم Visio إلى SVG|حشرة|
|DIAGRAMJAVA-50559|VSDM إلى VDX - الخطوط المتصلة غير متصلة بالأشكال|حشرة|
|DIAGRAMJAVA-50561|الرسم VSDX تالف بعد إضافة عنصر SolutionXML|حشرة|
### **يضيف SameAsPdfConversionArea في ImageSaveOptions**
تحدد ما إذا كان سيتم حفظ المنطقة بنفس طريقة حفظ المساحة PDF.

{{< highlight "java" >}}

 String dataDir = "C:\\temp\\";

// load a drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify image save options

ImageSaveOptions opts = new ImageSaveOptions(SaveFileFormat.PNG);

opts.setSameAsPdfConversionArea(true);

{{< /highlight >}}
