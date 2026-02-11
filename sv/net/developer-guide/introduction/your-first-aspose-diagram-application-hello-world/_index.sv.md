---
title: Din första Aspose.Diagram-ansökan - Hello World
type: docs
weight: 30
url: /sv/net/your-first-aspose-diagram-application-hello-world/
description: Den här sidan beskriver hur du skapar den första applikationen med biblioteket Aspose.Diagram.
---
{{% alert color="primary" %}}

Denna handledning visar hur man skapar en allra första applikation (Hello World) med Aspose.Diagram' simple API. Denna enkla applikation skapar en Microsoft Visio-fil med texten 'Hello World' på en specificerad sida.

{{% /alert %}}

## **Skapar Hello World-applikationen**

Stegen nedan skapar Hello World-applikationen med hjälp av Aspose.Diagram API:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) klass.
1.  Om du har en licens, då[tillämpa den](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Om du använder utvärderingsversionen, hoppa över de licensrelaterade kodraderna.
1. Skapa en ny Visio-fil eller öppna en befintlig Visio-fil.
1. Skapa en ny textruta.
1.  Sätt in orden**Hello World!** i en textruta.
1. Generera den modifierade filen Microsoft Visio.

Implementeringen av stegen ovan visas i exemplen nedan.

### **Kodexempel: Skapa en ny Diagram**

Följande exempel skapar en ny diagram från början, skriver Hello World! på första sidan och sparar filen Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


### **Kodexempel: Öppna en befintlig fil**

Följande exempel öppnar en befintlig Microsoft Visio mallfil med namnet "Sample.vsdx", matar in "Hello World!" text på första sidan och sparar diagram.


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

