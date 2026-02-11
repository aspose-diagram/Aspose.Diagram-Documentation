---
title: تحديد الهوامش
type: docs
weight: 20
url: /ar/java/setting-margins/
description: يوضح هذا القسم كيفية تعيين خيارات صفحة visio باستخدام Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram يدعم خيارات إعداد الصفحة Microsoft Visio بالكامل. قد يحتاج المطورون إلى تكوين إعدادات إعداد الصفحة للصفحات للتحكم في عملية الطباعة. يناقش هذا الموضوع كيفية استخدام Aspose.Diagram لتكوين هوامش الصفحة.

{{% /alert %}}

## **تحديد الهوامش**

 Aspose.Diagram يوفر فصل دراسي ،[**صفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) ، هذا يمثل ملف Microsoft Visio. ال[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تحتوي على[**الصفحات**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection) مجموعة تتيح الوصول إلى كل صفحة في ملف Visio. يتم تمثيل الصفحة بواسطة[**صفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)صف دراسي.

 ال[**ورقة الصفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) فئة توفر[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) الخاصية المستخدمة لتعيين خيارات إعداد الصفحة للصفحة. في الواقع ، هذا[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps) الخاصية هي كائن من[**ورقة الصفحة**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet) فئة تستخدم لتعيين خيارات تخطيط صفحة مختلفة لصفحة مطبوعة. ال[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)توفر فئة الخصائص المختلفة المستخدمة لتعيين خيارات إعداد الصفحة. تمت مناقشة بعض هذه الخصائص أدناه.

### **هوامش الصفحة**

 تعيين هوامش الصفحة (PageTopMargin و PageBottomMargin و PageLeftMargin و PageRightMargin) باستخدام[**PrintProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)أعضاء الفصل. يتم سرد بعض الطرق أدناه والتي تُستخدم لتحديد هوامش الصفحة:

- [**PageTopMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageTopMargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageBottomMargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageLeftMargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PageRightMargin)



{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageLeftMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageRightMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageTopMargin().setValue( 0.01);
diagram.getPages().get(0).getPageSheet().getPrintProps().getPageBottomMargin().setValue( 0.01);
{{< /highlight >}}
