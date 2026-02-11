---
title: Utilizzo della forma del tipo di connettore
type: docs
weight: 70
url: /it/net/working-with-connector-type-shape/
description: Questa sezione spiega come impostare l'aspetto del connettore con Aspose.Diagram.
---
## **Impostare l'aspetto della forma del tipo di connettore in Visio**
Questo argomento illustra in che modo gli sviluppatori possono modificare l'aspetto della forma del tipo di connettore dinamico utilizzando Aspose.Diagram for .NET.
### **Imposta l'aspetto del connettore**
 Il metodo SetConnectorsType esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzata per impostare l'aspetto della forma del tipo di connettore.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una particolare forma del connettore.
1. impostare l'aspetto della forma.
1. salvo diagram
#### **Esempio di programmazione dell'aspetto del connettore**
Utilizzare il seguente codice nell'applicazione .NET per impostare l'aspetto della forma del tipo di connettore utilizzando Aspose.Diagram for .NET.


{{< highlight csharp >}}
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

## **Selezionare l'opzione di reindirizzamento della forma del connettore**
 La proprietà ConFixedCode esposta da[Disposizione](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) la classe può essere utilizzata per selezionare l'opzione di reinstradamento. La proprietà Layout, esposta da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, verrà utilizzato.

Il codice seguente mostra come:

1. Carica un file di esempio.
1. ottenere una pagina particolare.
1. ottenere una particolare forma del connettore.
1. impostare le opzioni di reindirizzamento.
1. salvo diagram.
### **Selezionare Esempio di programmazione dell'opzione di reindirizzamento**
Utilizzare il seguente codice nell'applicazione .NET per selezionare l'opzione di reinstradamento della forma del connettore utilizzando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

