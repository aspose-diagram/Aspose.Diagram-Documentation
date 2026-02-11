---
title: تحقق من توسيع الصفحة تلقائيًا
type: docs
weight: 10
url: /ar/net/check-page-autoexpand/
description: يشرح هذا القسم كيفية التحقق أو تغيير الصفحة التي يتم توسيعها تلقائيًا في ملف visio مع Aspose.Diagram.
---
## **تغيير حجم الصفحة**

 ال[صفحة](http://www.aspose.com/api/net/diagram/aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.
 ال[PageProps](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/pageprops) يمثل الكائن سمات الصفحة ، مثل عرض الصفحة وارتفاعها ومقياسها. يمكن استخدام هذه الخاصية للتحقق من التوسيع التلقائي للصفحة.

استخدم خاصية PageProps للتحقق من التوسيع التلقائي للصفحة.
### **تعيين عينة برمجة حجم الصفحة**
التوسيع التلقائي لصفحة التحقق من الرمز التالي من diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Get Page autoexpand
bool isAutoExpand = page.PageSheet.PageProps.DrawingResizeType.Value == DrawingResizeTypeValue.Automatically ? true : false;
//Set Page autoexpand
page.PageSheet.PageProps.DrawingResizeType.Value = DrawingResizeTypeValue.NotAutomatically;

// Save Visio
diagram.Save(dataDir + "SetAutoExpand_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

