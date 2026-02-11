---
title: Ottieni Visio Forma Eredita caratteri
type: docs
weight: 101
url: /it/net/get-visio-shape-inherit-chars/
description: Questa sezione spiega come ottenere lo stile del carattere della forma visio ereditato dal suo stile genitore e master con Aspose.Diagram.
---
### **Recupera i dati dei caratteri ereditati di una forma Visio**
 Le forme Visio possono ereditare lo stile padre e la forma master. Gli sviluppatori possono ottenere o impostare i dati del carattere ereditato di una forma Visio. La proprietà InheritLine, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene i valori di formattazione della linea per la forma ereditata dallo stile genitore e dalla forma principale.
#### **Recupera esempio di programmazione dei dati dei caratteri ereditati**
Il frammento di codice seguente recupera i dati dei caratteri ereditati della forma. Si prega di controllare questo codice di esempio:


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


