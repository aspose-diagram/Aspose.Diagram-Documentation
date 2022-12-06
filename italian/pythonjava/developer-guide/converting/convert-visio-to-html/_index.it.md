---
title:  Converti Visio in formato HTML
linktitle: Converti Visio in HTML
type: docs
weight: 30
url: /it/python-java/convert-visio-to-html/
description: This topic show you how to convert Visio to html formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to html with a few lines of code.
---
## **Esporta Visio in HTML** ##
 Questo articolo spiega come esportare un Microsoft Visio diagram in HTML utilizzando[Aspose.Diagram per Python tramite Java](https://products.aspose.com/diagram/python-java/) API.

Usare il costruttore della classe Diagram per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato. Gli sviluppatori possono salvare l'HTML risultante nella memoria locale o direttamente in un'istanza di flusso.

 L'immagine sotto mostra a[VSD fascicolo](ExportToHTML.vsd)sta per essere salvato in formato PNG. È possibile utilizzare anche altri formati diagram (VSDX, VSTM, VSTM, VSSX, VSS, VSSM, VDX, VST, VSTX, VDX, VTX o 03.4811)

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToHTML.py" >}}



### **Salva l'HTML risultante in un'istanza di flusso**
È per caso d'uso salvare l'HTML risultante in un database o in un repository senza memorizzarlo nella memoria locale. Questa funzione incorpora anche altre risorse risultanti dell'HTML, ad esempio caratteri, CSS (contenenti le informazioni sullo stile) e immagini. Poiché salva un singolo file HTML nell'istanza del flusso.
#### **Salva l'HTML risultante in un esempio di programmazione del flusso**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportHTMLinStream.py" >}}
