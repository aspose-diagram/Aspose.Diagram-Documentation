---
title: Aggiorna i dati delle forme
type: docs
weight: 40
url: /it/net/refresh-shapes-data/
description: Questa sezione spiega come aggiornare i dati della forma per una forma visio con Aspose.Diagram.
---
## **Aggiorna la posizione della forma, inclusi xform, connection e geom quando si modifica il testo della forma o di altri**
 Il metodo RefreshData esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzata per aggiornare i dati della forma

Il codice seguente mostra come:

1. Carica un file di esempio.
1. Accedi a una forma particolare.
1. Aggiorna i dati della forma.
### **Aggiorna i dati di Shape**
Utilizzare il seguente codice nell'applicazione .NET per aggiornare una forma utilizzando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


