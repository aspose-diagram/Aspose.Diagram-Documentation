---
title:  Converti Visio in formato HTML
linktitle: Converti Visio in HTML
type: docs
weight: 30
url: /it/java/convert-visio-to-html/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in formati html. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in html con poche righe di codice.
---
## **Esporta Visio in HTML** **Esporta Visio in HTML**
 Questo articolo spiega come esportare un Microsoft Visio diagram in HTML utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) costruttore di classe per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato. Gli sviluppatori possono salvare l'HTML risultante nella memoria locale o direttamente in un'istanza di flusso.

1. [Salva l'HTML risultante nella memoria locale](/diagram/it/java/how-to-convert-a-visio-diagram/).
1. [Salva l'HTML risultante in un'istanza di flusso](/diagram/it/java/how-to-convert-a-visio-diagram/).

L'immagine sotto mostra un file VSD che sta per essere salvato in formato PNG. È possibile utilizzare altri formati diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX o VTX)1

**Inserisci diagram.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/YX4BNNq.png)

Per esportare VSD diagram in HTML, procedere come segue:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save della classe Dagram e imposta HTML come formato di output.

L'immagine seguente mostra il file HTML di output.

**Uscita HTML diagram.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/syavUqI.png)
### **Salva l'HTML risultante nella memoria locale**
Il file risultante può essere salvato passando una stringa di percorso completa, inclusi il nome file e l'estensione, ad esempio @"c:\temp\MyOutput.html".
#### **Salva l'HTML risultante nell'esempio di programmazione dell'archiviazione locale**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToHTML-ExportToHTML.java" >}}



### **Salva l'HTML risultante in un'istanza di flusso**
È per caso d'uso salvare l'HTML risultante in un database o in un repository senza memorizzarlo nella memoria locale. Questa funzione incorpora anche altre risorse risultanti dell'HTML, ad esempio caratteri, CSS (contenenti le informazioni sullo stile) e immagini. Poiché salva un singolo file HTML nell'istanza del flusso.
#### **Salva l'HTML risultante in un esempio di programmazione del flusso**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportHTMLinStream-ExportHTMLinStream.java" >}}
