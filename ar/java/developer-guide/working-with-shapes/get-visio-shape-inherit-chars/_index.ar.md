---
title: احصل على Visio Shape Inherit Chars
type: docs
weight: 101
url: /ar/java/get-visio-shape-inherit-chars/
description: يشرح هذا القسم كيفية الحصول على نمط خط الشكل visio الموروث من نمطه الرئيسي والمتقن باستخدام Aspose.Diagram.
---
### **استرجع بيانات الخط الموروثة لشكل Visio**
 يمكن أن ترث أشكال Visio النمط الأصل والشكل الرئيسي. يمكن للمطورين الحصول على بيانات الخط الموروثة لشكل Visio أو تعيينها. خاصية InheritChars ، المكشوفة بواسطة[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class ، تحتوي على قيم الخط للشكل الذي يرثه النمط الأصل والشكل الرئيسي.
#### **استرجاع نموذج برمجة بيانات الخط الموروث**
يسترد مقتطف التعليمات البرمجية التالي بيانات الخط الموروثة للشكل. يرجى التحقق من نموذج الكود هذا:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedChars.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
//Get Inherit Chars from the parent style and master
CharCollection chars = shape.getInheritChars();
for (int j = 0; j < chars.getCount(); j++) 
{
	Char ch = chars.get(j);
	System.out.println(ch.getColor().getValue());
	System.out.println(ch.getColorTrans().getValue());
	System.out.println(ch.getFontScale().getValue());
	System.out.println(ch.getSize().getValue());
	System.out.println(ch.getStyle().getValue());
	System.out.println(ch.getFontName().getValue());
	System.out.println(ch.isBold());
	System.out.println(ch.isDoubleStrikethrough());
	System.out.println(ch.isDoubleUnderline());
	System.out.println(ch.isItalic());
	System.out.println(ch.isStrikethrough());
	System.out.println(ch.isSubscript());
	System.out.println(ch.isSuperscript());
	System.out.println(ch.isUnderline());
}

{{< /highlight >}}




