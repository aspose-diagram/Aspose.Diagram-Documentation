---
title: احصل على Visio Shape Inherit Chars
type: docs
weight: 101
url: /ar/net/get-visio-shape-inherit-chars/
description: يشرح هذا القسم كيفية الحصول على نمط خط الشكل visio الموروث من نمطه الرئيسي والمتقن باستخدام Aspose.Diagram.
---
### **استرجع بيانات الخط الموروثة لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات الخط الموروثة لشكل Visio أو تعيينها. الخاصية InheritLine ، المكشوفة بواسطة[شكل](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class ، تحتوي على قيم تنسيق الخط للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
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
	Aspose.Diagram.Char ch = shape.InheritChars.GetChar(0);
	Console.WriteLine(ch.Style.Value);
	Console.WriteLine(ch.Color.Value); 
	Console.WriteLine(ch.FontName.Value); 
	Console.WriteLine(ch.Size.Value);
	Console.WriteLine(ch.Case.Value);
	Console.WriteLine(ch.IsUnderline);
	Console.WriteLine(ch.IsItalic);
	Console.WriteLine(ch.IsStrikethrough);
	Console.WriteLine(ch.IsDoubleStrikethrough);
	Console.WriteLine(ch.IsSubscript);
	Console.WriteLine(ch.IsSuperscript); 
}

{{< /highlight >}}


