---
title: تحويل شكل Visio إلى Html
type: docs
weight: 10
url: /ar/net/convert-a-visio-shape-to-html/
description: يشرح هذا القسم كيفية تحويل شكل visio إلى html باستخدام Aspose.Diagram.
---
## ** تحويل شكل visio إلى html**
 طريقة ToHTML التي كشفها ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يمكن استخدام class للتحويل إلى html.

يوضح الكود أدناه كيفية:

1. تحميل عينة diagram.
1. الحصول على صفحة معينة.
1. الحصول على شكل معين.
1. تحويل الشكل إلى html.
### **شكل إلى Html**
استخدم الكود التالي في تطبيق .net لتحويل شكل visio إلى html.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}
```

