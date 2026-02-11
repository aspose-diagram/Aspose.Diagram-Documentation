---
title: Aggiungi punto di connessione alla forma
type: docs
weight: 70
url: /it/net/add-connection-point-to-shape/
description: Questa sezione spiega come aggiungere un punto di connessione a una forma visio con Aspose.Diagram.
---
## **Aggiungi punto di connessione a una forma in Visio**
Questo argomento illustra come gli sviluppatori possono aggiungere un punto di connessione a una forma visio usando Aspose.Diagram for .NET.
### **Aggiungi punto di connessione**
 Il[Connessioni](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) L'oggetto rappresenta la raccolta di connessioni in[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. nuova connessione
1.  impostare la proprietà della connessione
1. aggiungi connessione alla forma
1. salvo diagram
#### **Aggiungi punto di connessione alla forma Esempio di programmazione**
Utilizzare il seguente codice nell'applicazione .NET per aggiungere la connessione a una forma utilizzando Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
