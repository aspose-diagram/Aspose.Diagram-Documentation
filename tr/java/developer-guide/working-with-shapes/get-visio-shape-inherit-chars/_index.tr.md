---
title: Visio Şekil Devralma Karakterlerini Alın
type: docs
weight: 101
url: /tr/java/get-visio-shape-inherit-chars/
description: Bu bölüm, visio şeklinin ana stilinden ve Aspose.Diagram ana stilinden devralınan yazı tipi stilinin nasıl alınacağını açıklar.
---
### **Visio Şeklinin Miras Alınan Yazı Tipi Verilerini Alma**
 Visio şekilleri, ana stili ve ana şekli devralabilir. Geliştiriciler, bir Visio şeklinin miras alınan yazı tipi verilerini alabilir veya ayarlayabilir. Tarafından sunulan InheritChars özelliği[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, üst stil ve ana şekil tarafından devralınan şeklin yazı tipi değerlerini içerir.
#### **Miras Alınan Yazı Tipi Verilerini Al Programlama Örneği**
Aşağıdaki kod parçacığı, şeklin devralınan yazı tipi verilerini alır. Lütfen bu örnek kodu kontrol edin:


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




