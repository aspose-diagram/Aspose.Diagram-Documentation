---
title: تغيير حجم الصفحة
type: docs
weight: 10
url: /ar/net/change-page-size/
description: يشرح هذا القسم كيفية تغيير حجم الصفحة في ملف visio باستخدام Aspose.Diagram.
---
## **تغيير حجم الصفحة**

 ال[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.
 ال[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) يمثل الكائن سمات الصفحة ، مثل عرض الصفحة وارتفاعها ومقياسها. يمكن استخدام هذه الخاصية لتغيير حجم الصفحة.

استخدم خاصية PageProps لتغيير حجم الصفحة.
### **تعيين عينة برمجة حجم الصفحة**
قطعة الكود التالية تغير حجم الصفحة من diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Set Page Size
page.PageSheet.PageProps.PageHeight.Value = 8;
page.PageSheet.PageProps.PageWidth.Value = 11;

// Save Visio
diagram.Save(dataDir + "SetPageSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
