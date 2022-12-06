---
title: Aspose.Diagram for Java 17.8 ملاحظات الإصدار
type: docs
weight: 50
url: /ar/java/aspose-diagram-for-java-17-8-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.8](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-8-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50412|أشكال مفقودة عند تحويل VST إلى PNG.|حشرة|
|DIAGRAMJAVA-50497|المخرج VSDX - تخطيط غير صحيح لجميع الخطوط المتصلة.|حشرة|
|DIAGRAMJAVA-50500|الناتج VSDX - لم يتم تغيير حجم الشكل المضاف يدويًا.|حشرة|
|DIAGRAMJAVA-50511|الإخراج VSDX - نص في غير مكانه للموصل الديناميكي.|حشرة|
|DIAGRAMJAVA-50516|المخرج VSDX - خط التوصيل الذي يمر عبر شكل آخر.|حشرة|
|DIAGRAMJAVA-50517|الناتج VSDX - أصبح شكل القرار أكبر.|حشرة|
|DIAGRAMJAVA-50520|لا يمكن تعيين سلوك التداخل لربط الخطوط في رسم VSDX.|حشرة|
|DIAGRAMJAVA-50521|الإخراج VSDX - تخطيط غير صحيح لخط الموصل.|حشرة|
|DIAGRAMJAVA-50522|إخراج PNG - يخرج نص الشكل عن الحدود.|حشرة|
|DIAGRAMJAVA-50523|الخرج VSDX - تخطيط غير صحيح لخط التوصيل.|حشرة|
|DIAGRAMJAVA-50525|الناتج VSDX - لا يتم الاحتفاظ بصيغة العرض لأي شكل.|حشرة|
|DIAGRAMJAVA-50528|الناتج VSDX - حجم غير صحيح للشكل.|حشرة|
|DIAGRAMJAVA-50529|الإخراج VSDX - الاحتفاظ بصيغ مقطع تحويل النص.|حشرة|
|DIAGRAMJAVA-50531|المخرج VSDX - لا يتناسب تخطيط الأشكال مع العرض والارتفاع في ورقة الأشكال.|حشرة|
|DIAGRAMJAVA-50533|الخرج VSDX - تخطيط غير صحيح لخط التوصيل.|حشرة|
## **API العام والتغييرات غير المتوافقة مع الإصدارات السابقة**
راجع قائمة أي تغييرات تم إجراؤها على API العام مثل الأعضاء المضافين أو المعاد تسميتهم أو المحذوفين أو المهملين بالإضافة إلى أي تغيير غير متوافق مع الإصدارات السابقة تم إجراؤه على Aspose.Diagram for Java. إذا كانت لديك مخاوف بشأن أي تغيير مدرج ، فيرجى رفعه على[Aspose.Diagram منتدى الدعم](https://forum.aspose.com/c/diagram/17).
### **يضيف عضو الجودة في فئة SVGSaveOptions**
يحصل أو يحدد قيمة تحدد جودة الصور التي تم إنشاؤها.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// specify SVG export settings

SVGSaveOptions options = new SVGSaveOptions();

// set image quality

options.setQuality(100);

// save drawing in the SVG format

diagram.save(dataDir + "UseSVGSaveOptions_out.svg", options);

{{< /highlight >}}
### **يضيف طريقة connectShapesViaConnectorIndex في فئة الصفحة**
يسمح بتوصيل الأشكال باستخدام فهارس الاتصال.

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Load an existing drawing

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get shapes by ID

Shape shape1 = diagram.getPages().get(0).getShapes().getShape(1);

Shape shape2 = diagram.getPages().get(0).getShapes().getShape(2);

// add connector shapes

Shape connector1 = new Shape();

long connecter1Id = diagram.addShape(connector1, "Dynamic connector", 0);

// connect shapes by index of conneecting points

diagram.getPages().get(0).connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

// save drawing

diagram.save(dataDir + "UseSVGSaveOptions_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [استخدم فهارس الاتصال لتوصيل الأشكال](https://docs.aspose.com/diagram/java/working-with-visio-shape-data/#use-connection-indexes-to-connect-shapes-programming-sample)
1. [استخدام SVG Save Options](https://docs.aspose.com/diagram/java/save-visio-document/#use-of-the-svg-save-options)
