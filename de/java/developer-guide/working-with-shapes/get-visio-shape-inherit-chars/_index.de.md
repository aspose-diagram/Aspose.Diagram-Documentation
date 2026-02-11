---
title: Holen Sie sich Visio Form erben Zeichen
type: docs
weight: 101
url: /de/java/get-visio-shape-inherit-chars/
description: In diesem Abschnitt wird erläutert, wie Sie den Schriftstil der visio-Form erhalten, der von seinem übergeordneten Stil geerbt und mit Aspose.Diagram gemastert wird.
---
### **Rufen Sie geerbte Schriftdaten einer Visio-Form ab**
 Die Formen Visio können den übergeordneten Stil und die Masterform erben. Entwickler können die Schriftartdaten einer Visio-Form abrufen oder festlegen. Die InheritChars-Eigenschaft, verfügbar gemacht durch die[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klasse, enthält die Schriftartwerte für die Form, die vom übergeordneten Stil und der Masterform geerbt wird.
#### **Programmierbeispiel für geerbte Schriftdaten abrufen**
Der folgende Codeausschnitt ruft die geerbten Schriftartdaten der Form ab. Bitte überprüfen Sie diesen Beispielcode:

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



