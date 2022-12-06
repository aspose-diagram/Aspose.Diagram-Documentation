---
title:  Converti Visio in formato HTML
linktitle: Converti Visio in HTML
type: docs
weight: 30
url: /it/net/convert-visio-to-html/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in formati html. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in html con poche righe di codice.
---
## **Esporta Visio in HTML**
 Questo articolo spiega come esportare un Microsoft Visio diagram in HTML utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) costruttore di classe per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato. Gli sviluppatori possono salvare l'HTML risultante nella memoria locale o direttamente in un'istanza di flusso.

1. [Salva l'HTML risultante nella memoria locale](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-the-local-storage).
1. [Salva l'HTML risultante in un'istanza di flusso](https://docs.aspose.com/diagram/net/convert-visio-to-html/#save-resultant-html-in-a-stream-instance).

L'immagine sotto mostra un file VSD che sta per essere salvato in formato PNG. È possibile utilizzare altri formati diagram (VSDX, VSDM, VSTX, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX o VTX)1

|**Inserisci diagram.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_6.png)|
Per esportare VSD diagram in HTML, procedere come segue:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save della classe Dagram e imposta HTML come formato di output.
### **Salva l'HTML risultante nella memoria locale**
Il file risultante può essere salvato passando una stringa di percorso completa, inclusi il nome file e l'estensione, ad esempio @"c:\temp\MyOutput.html".
#### **Salva l'HTML risultante nell'esempio di programmazione dell'archiviazione locale**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToHTML-ExportToHTML.cs" >}}



### **Salva l'HTML risultante in un'istanza di flusso**
È per caso d'uso salvare l'HTML risultante in un database o in un repository senza memorizzarlo nella memoria locale. Questa funzione incorpora anche altre risorse risultanti dell'HTML, ad esempio caratteri, CSS (contenenti le informazioni sullo stile) e immagini. Poiché salva un singolo file HTML nell'istanza del flusso.
#### **Salva l'HTML risultante in un esempio di programmazione del flusso**
{{< highlight "java" >}}

 // Load an existing visio diagram

Diagram diagram = new Diagram("Basic Flowchart.vsd");

// Save resultant HTML directly to a stream

MemoryStream stream = new MemoryStream();

diagram.Save(stream, SaveFileFormat.HTML);



{{< /highlight >}}
