---
title: Hello World Esempio
type: docs
weight: 90
url: /it/net/hello-world-example/
description: Questa pagina descrive come creare un esempio di hello world con la libreria Aspose.Diagram.
---
## **Hello World Esempio**
Aspose.Diagram for .NET has rich features to create, open, edit and convert Microsoft Visio files using C# and other .NET languages. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

Dopo[installazione Aspose.Diagram for .NET](/diagram/it/net/installation/)nel proprio ambiente, è possibile utilizzare i seguenti passaggi per vedere come Aspose.Diagram API viene utilizzato nelle applicazioni .NET.

1. Crea un'istanza di un oggetto Diagram
1. Utilizzare il metodo Save dell'oggetto di classe Diagram per salvare il file su disco

The following code snippet is a Hello World program to exhibit the working of Aspose.Diagram for .NET API. 

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




