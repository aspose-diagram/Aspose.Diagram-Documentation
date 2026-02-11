---
title: تحديد الهوامش
type: docs
weight: 20
url: /ar/net/setting-margins/
description: يوضح هذا القسم كيفية تعيين خيارات صفحة visio باستخدام Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram يدعم خيارات إعداد الصفحة Microsoft Visio بالكامل. قد يحتاج المطورون إلى تكوين إعدادات إعداد الصفحة للصفحات للتحكم في عملية الطباعة. يناقش هذا الموضوع كيفية استخدام Aspose.Diagram لتكوين هوامش الصفحة.

{{% /alert %}}

## **تحديد الهوامش**

 Aspose.Diagram يوفر فصل دراسي ،[**صفحة**](https://reference.aspose.com/diagram/net/aspose.diagram/page) ، هذا يمثل ملف Microsoft Visio. ال[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page) فئة تحتوي على[**الصفحات**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) مجموعة تتيح الوصول إلى كل صفحة في ملف Visio. يتم تمثيل الصفحة بواسطة[**صفحة**](https://reference.aspose.com/diagram/net/aspose.diagram/page)صف دراسي.

 ال[**ورقة الصفحة**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) فئة توفر[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) الخاصية المستخدمة لتعيين خيارات إعداد الصفحة للصفحة. في الواقع ، هذا[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops) الخاصية هي كائن من[**ورقة الصفحة**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet) فئة تستخدم لتعيين خيارات تخطيط صفحة مختلفة لصفحة مطبوعة. ال[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)توفر فئة الخصائص المختلفة المستخدمة لتعيين خيارات إعداد الصفحة. تمت مناقشة بعض هذه الخصائص أدناه.

### **هوامش الصفحة**

 تعيين هوامش الصفحة (PageTopMargin و PageBottomMargin و PageLeftMargin و PageRightMargin) باستخدام[**PrintProps**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)أعضاء الفصل. يتم سرد بعض الطرق أدناه والتي تُستخدم لتحديد هوامش الصفحة:

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**PageBottomMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**PageLeftMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**PageRightMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set Page Margin
diagram.Pages[0].PageSheet.PrintProps.PageLeftMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageRightMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageTopMargin.Value = 0.01;
diagram.Pages[0].PageSheet.PrintProps.PageBottomMargin.Value = 0.01;
{{< /highlight >}}
