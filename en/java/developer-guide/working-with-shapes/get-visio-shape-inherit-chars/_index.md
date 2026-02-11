---
title: Get Visio Shape Inherit Chars
type: docs
weight: 101
url: /java/get-visio-shape-inherit-chars/
description: This section explains how to get visio shape's font style inherited from it's parent style and master with Aspose.Diagram.
---
### **Retrieve Inherited Font Data of a Visio Shape**
The Visio shapes can inherit the parent style and the master shape. Developers may get or set the inherit font data of a Visio shape. The InheritChars property, exposed by the [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contains the font values for the shape inherit by the parent style and the master shape.
#### **Retrieve Inherited Font Data Programming Sample**
The following code snippet retrieves the inherited font data of the shape. Please check this sample code:


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




