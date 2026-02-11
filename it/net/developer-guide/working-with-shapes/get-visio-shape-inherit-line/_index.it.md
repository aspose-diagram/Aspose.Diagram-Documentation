---
title: Ottieni Visio Shape Eredita linea
type: docs
weight: 100
url: /it/net/get-visio-shape-inherit-line/
description: Questa sezione spiega come ottenere lo stile di linea della forma visio ereditato dal suo stile genitore e master con Aspose.Diagram.
---
### **Recupera dati linea ereditati di una forma Visio**
 Le forme Visio possono ereditare lo stile padre e la forma master. Gli sviluppatori possono ottenere o impostare i dati della linea ereditata di una forma Visio. La proprietà InheritLine, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene i valori di formattazione della linea per la forma ereditata dallo stile genitore e dalla forma principale.
#### **Recupera esempio di programmazione dei dati della riga ereditata**
Il frammento di codice seguente recupera i dati della linea ereditati della forma. Si prega di controllare questo codice di esempio:


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
	Line line = shape.InheritLine;
	Console.WriteLine(line.LinePattern.Value);
	Console.WriteLine(line.LineColor.Value);
	Console.WriteLine(line.BeginArrow.Value);
	Console.WriteLine(line.BeginArrowSize.Value);
	Console.WriteLine(line.EndArrow.Value);
	Console.WriteLine(line.EndArrowSize.Value);
	Console.WriteLine(line.LineWeight.Value);
}

{{< /highlight >}}


