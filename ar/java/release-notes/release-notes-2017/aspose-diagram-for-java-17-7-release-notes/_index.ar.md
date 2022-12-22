---
title: Aspose.Diagram for Java 17.7 ملاحظات الإصدار
type: docs
weight: 60
url: /ar/java/aspose-diagram-for-java-17-7-release-notes/
---
{{% alert color="primary" %}} 

 تحتوي هذه الصفحة على ملاحظات الإصدار لـ[Aspose.Diagram for Java 17.7](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-17-7-release-notes/).

{{% /alert %}} 
## **التحسينات والتغييرات**

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50491|لا يمكن استرداد ارتفاع الشكل الجديد المصاغ.|التعزيز|
|DIAGRAMJAVA-50510|VSD إلى SVG - نموذج لون تعبئة غير صحيح في الأشكال.|التعزيز|
|DIAGRAMJAVA-50483|اتصال غير كامل للأشكال عند حفظ رسم بتنسيق VSDX.|حشرة|
|DIAGRAMJAVA-50488|تتم إضافة عناصر نصية إضافية عند تحويل VSD إلى SVG.|حشرة|
|DIAGRAMJAVA-50490|تكون خطوط الحدود العمودية لمربع العملية المحدد مسبقًا سميكة عند إنشاء رسم VSDX.|حشرة|
|DIAGRAMJAVA-50495|الإخراج VSDX - تخطيط غير صحيح لخط الموصل عند إضافة نص إلى الأشكال.|حشرة|
|DIAGRAMJAVA-50496|الخرج VSDX - جميع الموصلات تنجرف لأعلى.|حشرة|
|DIAGRAMJAVA-50498|الناتج VSDX - عرض نص رأسي للأشكال بدلاً من الأفقي.|حشرة|
|DIAGRAMJAVA-50506|حدث خطأ أثناء تحميل رسم VDX.|حشرة|
|DIAGRAMJAVA-50508|المخرج VSDX - تجاوز النص عند إضافة نص متعدد الأسطر.|حشرة|
|DIAGRAMJAVA-50511|الإخراج VSDX - نص في غير مكانه للموصل الديناميكي.|حشرة|
|DIAGRAMJAVA-50512|المخرج VSDX - خط التوصيل الذي يمر عبر شكل آخر|حشرة|
|DIAGRAMJAVA-50513|المخرج VSDX - خط إضافي للموصل داخل شكل القرار|حشرة|
|DIAGRAMJAVA-50515|المخرج VSDX - نص الشكل بأكمله خارج الحد|حشرة|
### **يتم إضافة طريقة addComment في فئة الصفحة**
تأخذ طريقة addComment المحملة بشكل زائد ، والتي يتم عرضها بواسطة فئة الصفحة ، مثيل فئة الشكل وسلسلة نصية للتعليق.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// retrieve page by name

Page page = diagram.getPages().getPage("Page-1");

// retrieve shape by ID

Shape shape = page.getShapes().getShape(12);

page.addComment(shape, "Hello");

// save diagram

diagram.save("c:\\temp\\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **أمثلة على الاستخدام**
يرجى التحقق من قائمة مواضيع المساعدة المضافة في Aspose.Diagram مستندات Wiki:

1. [أضف تعليقًا على مستوى الشكل في رسم Visio](/diagram/ar/java/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
