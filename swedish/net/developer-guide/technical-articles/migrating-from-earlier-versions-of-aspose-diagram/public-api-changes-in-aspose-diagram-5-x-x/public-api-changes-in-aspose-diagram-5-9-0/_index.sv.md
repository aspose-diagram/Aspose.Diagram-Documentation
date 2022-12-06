---
title: Offentlig API Ändringar i Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /sv/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.8.0 till 5.9.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
## **Spara resultatet HTML till en ström**
Den nya Spara-metoden har lagts till i klassen Diagram. Det krävs två parametrar, strömobjektet och filformatet för att spara.
Exempelkod:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Kopiera teman och sidblad från en annan Visio**
Klassen Diagram erbjuder CopyTheme-metoden och PageSheet-klassen erbjuder Copy-metoden för att uppnå målet att kopiera en form och andra manipulationsuppgifter.
 Exempelkoder:[Kopiera former från en befintlig Visio](/diagram/sv/net/add-retrieve-copy-and-read-visio-shape-data/)
## **VSTX och VSSX Sparningsalternativ läggs till i SaveFileFormat**
Tidigare hade Aspose.Diagram API stöd för läsning och skrivning VSDX, men nu har vi lagt till stöd för att skriva diagram i formaten VSTX och VSSX också. Exempelkoder:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX Läsalternativ läggs till i LoadFileFormat**
Tidigare hade Aspose.Diagram API stöd för läsning och skrivning i formatet VSDX, men nu har vi lagt till stöd för att läsa VSSX stencilformat också. Exempelkoder:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**VB**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
