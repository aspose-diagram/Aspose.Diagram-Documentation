---
title: Your First Aspose.Diagram Application - Hello World
type: docs
weight: 30
url: /de/net/your-first-aspose-diagram-application-hello-world/
description: Auf dieser Seite wird beschrieben, wie Sie die erste Anwendung mit der Bibliothek Aspose.Diagram erstellen.
---
{{% alert color="primary" %}}

This tutorial shows how to create a very first application (Hello World) using Aspose.Diagram' simple API. This simple application creates a Microsoft Visio file with the text 'Hello World' in a specified Page.

{{% /alert %}}

## **Creating the Hello World Application**

The steps below creates the Hello World application using the Aspose.Diagram API:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) Klasse.
1.  Wenn Sie eine Lizenz haben, dann[Wende es an](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Wenn Sie die Evaluierungsversion verwenden, überspringen Sie die lizenzbezogenen Codezeilen.
1. Erstellen Sie eine neue Visio-Datei oder öffnen Sie eine vorhandene Visio-Datei.
1. Erstellen Sie ein neues Textfeld.
1.  Füge die Wörter ein**Hello World!** in ein Textfeld.
1. Generieren Sie die geänderte Datei Microsoft Visio.

Die Implementierung der obigen Schritte wird in den folgenden Beispielen demonstriert.

### **Codebeispiel: Erstellen einer neuen Diagram**

The following example creates a new diagram from the scratch, writes Hello World! on the first page and saves the Visio file.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


### **Codebeispiel: Öffnen einer vorhandenen Datei**

The following example opens an existing Microsoft Visio template file named "Sample.vsdx", inputs "Hello World!" text in the first page and saves the diagram.


{{< highlight csharp >}}
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

