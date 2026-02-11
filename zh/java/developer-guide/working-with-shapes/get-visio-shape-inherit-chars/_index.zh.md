---
title: 获取 Visio 形状继承字符
type: docs
weight: 101
url: /zh/java/get-visio-shape-inherit-chars/
description: 本节介绍如何获取 visio 形状的字体样式从其父样式继承并掌握 Aspose.Diagram。
---
### **检索 Visio 形状的继承字体数据**
Visio 形状可以继承父样式和主形状。开发者可以获取或设置一个Visio形状的继承字体数据。 InheritChars 属性，由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类，包含由父样式和主形状继承的形状的字体值。
#### **检索继承的字体数据编程示例**
以下代码片段检索形状的继承字体数据。请检查此示例代码：

```
{{< highlight "java" >}}
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
```



