---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /it/net/your-first-aspose-diagram-application-hello-world/
description: Questa pagina descrive come creare la prima applicazione con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Crea un'istanza di[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) classe.
1.  Se hai una licenza, allora[applicarlo](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Se stai utilizzando la versione di valutazione, salta le righe di codice relative alla licenza.
1. Crea un nuovo file Visio o apri un file Visio esistente.
1. Crea una nuova casella di testo.
1.  Inserisci le parole**Hello World!** in una casella di testo.
1. Generare il file Microsoft Visio modificato.

L'implementazione dei passaggi precedenti è dimostrata negli esempi seguenti.

### **Esempio di codice: creazione di un nuovo Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

### **Esempio di codice: apertura di un file esistente**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
