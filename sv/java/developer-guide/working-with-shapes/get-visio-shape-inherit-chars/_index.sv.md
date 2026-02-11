---
title: Skaffa Visio Shape Inherit Chars
type: docs
weight: 101
url: /sv/java/get-visio-shape-inherit-chars/
description: Det här avsnittet förklarar hur du får visio-formens teckensnittsstil ärvd från dess överordnade stil och master med Aspose.Diagram.
---
### **Hämta ärvda teckensnittsdata för en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvte teckensnittsdata för en Visio-form. Egenskapen InheritChars, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, innehåller teckensnittsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt teckensnittsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda teckensnittsdata. Kontrollera denna exempelkod:

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



