---
title: Obtener Visio Forma Heredar caracteres
type: docs
weight: 101
url: /es/java/get-visio-shape-inherit-chars/
description: Esta sección explica cómo obtener el estilo de fuente de la forma visio heredado de su estilo principal y maestro con Aspose.Diagram.
---
### **Recuperar datos de fuente heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de fuente heredados de una forma Visio. La propiedad InheritChars, expuesta por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contiene los valores de fuente para la forma heredada por el estilo principal y la forma maestra.
#### **Ejemplo de programación de recuperación de datos de fuente heredados**
El siguiente fragmento de código recupera los datos de fuente heredados de la forma. Por favor revise este código de muestra:

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



