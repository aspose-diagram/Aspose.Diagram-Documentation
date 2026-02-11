---
title: Ottieni Visio Forma Eredita riempimento
type: docs
weight: 100
url: /it/net/get-visio-shape-inherit-fill/
description: Questa sezione spiega come ottenere lo stile di riempimento della forma visio ereditato dallo stile genitore e master con Aspose.Diagram.
---
### **Recupera i dati di riempimento ereditati di una forma Visio**
Le forme Visio possono ereditare lo stile padre e la forma principale. Gli sviluppatori possono ottenere i dati inherit Fill di una forma Visio. La proprietà InheritFill, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene i valori di formattazione del riempimento per la forma ereditata dallo stile principale e dalla forma principale.
#### **Esempio di programmazione dei dati di riempimento ereditati Recupera**
Il seguente frammento di codice recupera i dati di riempimento ereditati della forma. Si prega di controllare questo codice di esempio:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
	Fill f = shape.InheritFill;
	Console.WriteLine(f.FillForegnd.Value);
	Console.WriteLine(f.FillPattern.Value);
	Console.WriteLine(f.ShdwForegnd.Value);
	Console.WriteLine(f.ShdwPattern.Value);
}

{{< /highlight >}}
```

