---
title: Pubblico API Modifiche Aspose.Diagram 5.9.0
type: docs
weight: 10
url: /it/java/public-api-changes-in-aspose-diagram-5-9-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 5.8.0 alla 5.9.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Save Resultant HTML to a Stream**
Il nuovo metodo di salvataggio è stato aggiunto nella classe Diagram. Richiede due parametri, l'oggetto stream e il formato del file di salvataggio.
Codice di esempio:

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
### **Copia temi e foglio di pagina da un altro Visio**
La classe Diagram offre il metodo CopyTheme e la classe PageSheet offre il metodo Copy per raggiungere l'obiettivo di copiare una forma e altre attività di manipolazione.
 Esempi di codici:[Copia forme da un Visio esistente](/diagram/it/java/working-with-visio-shape-data/#copy-shapes-from-an-existing-visio)
### **VSTX e VSSX Le opzioni di salvataggio vengono aggiunte in SaveFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura e la scrittura del formato VSDX, ma ora abbiamo aggiunto il supporto per la scrittura di diagrammi anche nei formati VSTX e VSSX. Esempi di codici:

**Java**

{{< highlight "java" >}}

 // save diagram in the VSTX format

diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);

// save diagram in the VSSX format

diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);

{{< /highlight >}}
### **VSSX L'opzione di lettura viene aggiunta in LoadFileFormat**
In precedenza, Aspose.Diagram API supportava la lettura e la scrittura del formato VSDX, ma ora abbiamo aggiunto il supporto per la lettura anche del formato stencil VSSX. Esempi di codici:

**Java**

{{< highlight "java" >}}

 // read VSSX stencil

Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);

{{< /highlight >}}
