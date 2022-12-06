---
title: Offentlig API Ändringar i Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /sv/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Det här dokumentet beskriver ändringar av Aspose.Diagram API från version 5.8.0 till 5.9.0, som kan vara av intresse för modul-/applikationsutvecklare. Den innehåller inte bara nya och uppdaterade offentliga metoder, utan också en beskrivning av eventuella förändringar i beteendet bakom kulisserna i Aspose.Diagram.

{{% /alert %}} 
### **Spara resulterande HTML i en ström**
Den nya sparmetoden har lagts till i klassen Diagram. Det krävs två parametrar, strömobjektet och filformatet för att spara.
Exempelkod:

**Java**

{{< highlight "java" >}}

 // Call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

ByteArrayOutputStream dstStream = new ByteArrayOutputStream();

diagram.save(dstStream, SaveFileFormat.HTML);

// In you want to read the result into a Diagram object again, in Java you need to get the

// data bytes and wrap into an input stream.

ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());

{{< /highlight >}}
### **Kopiera teman och sidblad från en annan Visio**
Klassen Diagram erbjuder CopyTheme-metoden och PageSheet-klassen erbjuder Copy-metoden för att uppnå målet att kopiera en form och andra manipulationsuppgifter.
 Exempelkoder:[Kopiera former från en befintlig Visio](/diagram/sv/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX och VSSX Sparningsalternativ läggs till i SaveFileFormat**
Tidigare hade Aspose.Diagram API stöd för läsning och skrivning VSDX, men nu har vi lagt till stöd för att skriva diagram i formaten VSTX och VSSX också. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX Läsalternativ läggs till i LoadFileFormat**
Tidigare hade Aspose.Diagram API stöd för läsning och skrivning i formatet VSDX, men nu har vi lagt till stöd för att läsa VSSX stencilformat också. Exempelkoder:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
