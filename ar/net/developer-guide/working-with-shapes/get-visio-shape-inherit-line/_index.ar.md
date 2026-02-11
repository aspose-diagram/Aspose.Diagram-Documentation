---
title: احصل على Visio Shape Inherit Line
type: docs
weight: 100
url: /ar/net/get-visio-shape-inherit-line/
description: يشرح هذا القسم كيفية الحصول على نمط خط الشكل visio الموروث من النمط الأصلي والشكل الرئيسي باستخدام Aspose.Diagram.
---
### **استرجع بيانات الخط الموروث لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات خط التوريث لشكل Visio أو تعيينها. الخاصية InheritLine ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ، تحتوي على قيم تنسيق الخط للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات الخط الموروث**
يسترد مقتطف التعليمات البرمجية التالي بيانات الخط الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}


