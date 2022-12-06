---
title:  Converti Visio in formato PDF
linktitle: Converti Visio in PDF
type: docs
weight: 10
url: /it/python-net/convert-visio-to-pdf/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in formati PDF. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in PDF con poche righe di codice.
---
## **Esporta in PDF**
{{% alert color="primary" %}}

Aspose.Diagram per Python tramite .NET scrive direttamente le informazioni su API e il numero di versione nei documenti di output. Ad esempio, dopo il rendering di un disegno in PDF, Aspose.Diagram for .NET viene popolato**Applicazione** campo con valore 'Aspose.Diagram' e**Produttore PDF** campo con valore, ad esempio 'Aspose.Diagram 17.9'.

Si noti che non è possibile incaricare Aspose.Diagram for .NET API di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

 Questo articolo spiega come esportare un Microsoft Visio diagram in PDF utilizzando[Aspose.Diagram per Python tramite .NET](https://products.aspose.com/diagram/python-net/) API.

Utilizzare il costruttore di classe [Diagram] per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

L'immagine qui sotto mostra il VSD diagram che i frammenti di codice qui sotto esportano in PDF. Puoi utilizzare anche altri formati diagram (VSS, VSSM, VDX, VST, VSTX, VDX, VTX o VSX).

|**Il file sorgente.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_1.png)|


Per esportare VSD diagram in PDF:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save delle classi Diagram e imposta il formato di output su PDF.

Di seguito è riportata un'immagine del file PDF di output.

|**Il file PDF di output.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_2.png)|
### **Esporta Microsoft Visio Disegno in PDF**
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in PDF utilizzando Python.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}
