---
title: Hello World Exempel
type: docs
weight: 100
url: /sv/java/hello-world-example/
---
## **Hello World Exempel**
Ett "Hello World"-exempel används traditionellt för att introducera funktioner i ett programmeringsspråk eller programvara med ett enkelt användningsfall.

Aspose.Diagram for Java är en funktionsrik Visio filbehandling API som tillåter applikationsutvecklare att bädda in Visio dokumentskapande, läsning och konverteringsfunktioner i sina Java applikationer. It supports working with many popular Visio file-formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. The API has strong conversion features to convert Visio Diagrams to a number of format som PDF, HTML, XML, SVG och XAML.

Efter[installera Aspose.Diagram for Java](/diagram/sv/java/installation/)i din miljö kan du köra kodexemplet nedan för att se hur Aspose.Diagram API fungerar.

Nedanstående kodavsnitt följer dessa steg:

1. Instantiera ett Diagram-objekt
1. Använd metoden Spara för klassobjektet Diagram för att spara filen på skivan

Följande kodavsnitt är ett Hello World-program för att visa hur Aspose.Diagram for Java API fungerar.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}





