---
title: احصل على Visio Shape Inherit Fill
type: docs
weight: 100
url: /ar/net/get-visio-shape-inherit-fill/
description: يشرح هذا القسم كيفية الحصول على نمط تعبئة الشكل visio الموروث من النمط الأصل والشكل الرئيسي باستخدام Aspose.Diagram.
---
### **استرجع بيانات التعبئة الموروثة لشكل Visio**
يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. قد يحصل المطورون على بيانات التعبئة الموروثة لشكل Visio. الخاصية InheritFill ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ، تحتوي على قيم تنسيق التعبئة للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات التعبئة الموروثة**
يسترد مقتطف التعليمات البرمجية التالي بيانات التعبئة الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}
```

