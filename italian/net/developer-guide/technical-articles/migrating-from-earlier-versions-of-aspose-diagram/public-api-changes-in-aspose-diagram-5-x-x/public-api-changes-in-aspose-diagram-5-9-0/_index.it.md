---
title: Pubblico API Modifiche Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /it/net/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 5.8.0 alla 5.9.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
## **Salva l'HTML risultante in uno stream**
Il nuovo metodo Save è stato aggiunto nella classe Diagram. Richiede due parametri, l'oggetto stream e il formato del file di salvataggio.
Codice di esempio:

**C#**

{{< highlight "java" >}}

 // load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' load an existing visio diagram

Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream()

diagram.Save(stream, SaveFileFormat.HTML)

{{< /highlight >}}
## **Copia temi e foglio di pagina da un altro Visio**
La classe Diagram offre il metodo CopyTheme e la classe PageSheet offre il metodo Copy per raggiungere l'obiettivo di copiare una forma e altre attività di manipolazione.
 Esempi di codici:[Copia forme da un Visio esistente](/diagram/it/net/add-retrieve-copy-and-read-visio-shape-data/)
## **VSTX e VSSX Le opzioni di salvataggio vengono aggiunte in SaveFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura e la scrittura del formato VSDX, ma ora abbiamo aggiunto il supporto per la scrittura di diagrammi anche nei formati VSTX e VSSX. Esempi di codici:

**C#**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' save diagram in the VSTX format

diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)

' save diagram in the VSSX format

diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)

{{< /highlight >}}
## **VSSX L'opzione di lettura viene aggiunta in LoadFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura e la scrittura del formato VSDX, ma ora abbiamo aggiunto il supporto per la lettura anche del formato stencil VSSX. Esempi di codici:

**C#**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}

**V.B**

{{< highlight "java" >}}

 ' read VSSX stencil

Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)

{{< /highlight >}}
