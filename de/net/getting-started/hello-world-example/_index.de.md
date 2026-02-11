---
title: Hello World Beispiel
type: docs
weight: 90
url: /de/net/hello-world-example/
description: Auf dieser Seite wird beschrieben, wie Sie mit der Bibliothek Aspose.Diagram ein Beispiel für „Hello World“ erstellen.
---
## **Hello World Beispiel**
Aspose.Diagram for .NET has rich features to create, open, edit and convert Microsoft Visio files using C# and other .NET languages. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

Nach[Installation Aspose.Diagram for .NET](/diagram/de/net/installation/)In Ihrer Umgebung können die folgenden Schritte verwendet werden, um zu sehen, wie Aspose.Diagram API in .NET-Anwendungen verwendet wird.

1. Instanziieren Sie ein Diagram-Objekt
1. Verwenden Sie die Save-Methode des Klassenobjekts Diagram, um die Datei auf der Disc zu speichern

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




