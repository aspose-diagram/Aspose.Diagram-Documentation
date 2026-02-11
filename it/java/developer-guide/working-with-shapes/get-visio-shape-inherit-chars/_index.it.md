---
title: Ottieni Visio Forma Eredita caratteri
type: docs
weight: 101
url: /it/java/get-visio-shape-inherit-chars/
description: Questa sezione spiega come ottenere lo stile del carattere della forma visio ereditato dal suo stile genitore e master con Aspose.Diagram.
---
### **Recupera i dati dei caratteri ereditati di una forma Visio**
 Le forme Visio possono ereditare lo stile padre e la forma master. Gli sviluppatori possono ottenere o impostare i dati del carattere ereditato di una forma Visio. La proprietà InheritChars, esposta da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, contiene i valori del carattere per la forma ereditata dallo stile genitore e dalla forma master.
#### **Recupera esempio di programmazione dei dati dei caratteri ereditati**
Il frammento di codice seguente recupera i dati dei caratteri ereditati della forma. Si prega di controllare questo codice di esempio:


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




