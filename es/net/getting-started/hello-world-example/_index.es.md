---
title: Hello World Ejemplo
type: docs
weight: 90
url: /es/net/hello-world-example/
description: Esta página describe cómo crear un ejemplo de hola mundo con la biblioteca Aspose.Diagram.
---
## **Hello World Ejemplo**
Aspose.Diagram for .NET has rich features to create, open, edit and convert Microsoft Visio files using C# and other .NET languages. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of formats such as PDF, HTML, XML, SVG, and XAML.

Después[instalando Aspose.Diagram for .NET](/diagram/es/net/installation/)en su entorno, se pueden usar los siguientes pasos para ver cómo se utiliza Aspose.Diagram API en las aplicaciones .NET.

1. Crear una instancia de un objeto Diagram
1. Use el método Guardar del objeto de clase Diagram para guardar el archivo en el disco

The following code snippet is a Hello World program to exhibit the working of Aspose.Diagram for .NET API. 


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}





