---
title: Hello World Exempel
type: docs
weight: 90
url: /sv/net/hello-world-example/
description: Den här sidan beskriver hur man skapar exempel på hej världen med Aspose.Diagram-biblioteket.
---
## **Hello World Exempel**
Aspose.Diagram for .NET har rika funktioner för att skapa, öppna, redigera och konvertera Microsoft Visio filer med C# och andra .NET språk. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of format som PDF, HTML, XML, SVG och XAML.

Efter[installera Aspose.Diagram for .NET](/diagram/sv/net/installation/)i din miljö kan följande steg användas för att se hur Aspose.Diagram API används i .NET-applikationer.

1. Instantiera ett Diagram-objekt
1. Använd metoden Spara för klassobjektet Diagram för att spara filen på skivan

Följande kodavsnitt är ett Hello World-program för att visa hur Aspose.Diagram for .NET API fungerar.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}





