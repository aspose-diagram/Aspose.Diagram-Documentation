---
title: قم بتحديث بيانات الأشكال
type: docs
weight: 40
url: /ar/net/refresh-shapes-data/
description: يشرح هذا القسم كيفية تحديث بيانات الشكل لشكل visio باستخدام Aspose.Diagram.
---
## **تحديث موضع الشكل بما في ذلك xform والاتصال و geom عند تغيير نص الشكل أو نصوص أخرى**
 طريقة RefreshData التي كشف عنها ملف[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) يمكن استخدام class لتحديث بيانات الشكل

يوضح الكود أدناه كيفية:

1. تحميل ملف عينة.
1. الوصول إلى شكل معين.
1. قم بتحديث بيانات الشكل.
### **تحديث بيانات الشكل**
استخدم الكود التالي في تطبيق .NET لتحديث شكل باستخدام Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

