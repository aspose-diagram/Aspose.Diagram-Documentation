---
title: تغيير خصائص الطبقة
type: docs
weight: 130
url: /ar/net/change-properties-layer/
description: يوضح هذا القسم كيفية تغيير خصائص الطبقة باستخدام Aspose.Diagram.
---
## **تغيير خصائص الطبقة في Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يسمح بتغيير خصائص الطبقة في Microsoft Office Visio diagram يمكن أن ينتمي كل شكل إلى طبقات متعددة حتى يتمكن المطورون من تغيير خصائص الطبقة لتناسب احتياجات المستخدم النهائي. ال[ورقة الصفحة](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)يقدم كائن الفئة طبقات تسمح بإضافة كائنات طبقة وإزالتها في رسم Visio. يمكن للمستخدمين إدارة[طبقة](https://reference.aspose.com/diagram/net/aspose.diagram/layer) الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:
### **تغيير عينة برمجة خصائص الطبقة**
يساعد الجزء التالي من التعليمات البرمجية على تغيير خصائص الطبقة.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Layers();

// Load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the layers
foreach (Aspose.Diagram.Layer layer in Page.PageSheet.Layers)
{
    layer.Visible.Value = Aspose.Diagram.BOOL.True;
    layer.Print.Value = Aspose.Diagram.BOOL.True;
}
// Save diagram
diagram.Save(dataDir + "ChangeLayerProperty_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```