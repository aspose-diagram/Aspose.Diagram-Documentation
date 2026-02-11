---
title: احصل على عرض الورق وارتفاع الصفحة
type: docs
weight: 50
url: /ar/net/get-paper-width-and-height-of-page/
description: يوضح هذا القسم كيفية الحصول على حجم ورق لصفحة visio مع Aspose.Diagram.
---
## **سيناريوهات الاستخدام الممكنة**

في بعض الأحيان ، تحتاج إلى معرفة عرض وارتفاع حجم الورق حيث تم ضبطه في إعداد الصفحة للصفحة. الرجاء استخدام[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)و[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)خصائص لهذا الغرض.

## **الحصول على عرض الصفحة وارتفاع دعامة الصفحة**

 يشرح نموذج التعليمات البرمجية التالي استخدام[**PageProps.PageWidth**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pagewidth)و[**PageProps.PageHeight**](https://reference.aspose.com/diagram/net/aspose.diagram/pageprops/properties/pageheight)الخصائص.

### **عينة من الرموز**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");

// Get page's width and height
double pagewidth = page.PageSheet.PageProps.PageWidth.Value;
double pageheight = page.PageSheet.PageProps.PageHeight.Value;

{{< /highlight >}}
```
