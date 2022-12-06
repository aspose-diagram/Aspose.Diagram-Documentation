---
title:  Converti Visio in formato PDF
linktitle: Converti Visio in PDF
type: docs
weight: 10
url: /it/java/convert-visio-to-pdf/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in formati PDF. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in PDF con poche righe di codice.
---
## **Esportazione in PDF**
{{% alert color="primary" %}}

Aspose.Diagram for Java scrive direttamente le informazioni su API e il numero di versione nei documenti di output. Ad esempio, durante il rendering di un disegno in PDF, Aspose.Diagram for Java viene popolato**Applicazione**campo con valore 'Aspose.Diagram' e**Produttore PDF**campo con un valore, ad esempio 'Aspose.Diagram 17.9'.

Si noti che non è possibile incaricare Aspose.Diagram for Java API di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

 Questo articolo spiega come esportare un Microsoft Visio diagram in PDF utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

L'immagine qui sotto mostra il VSD diagram che i frammenti di codice qui sotto esportano in PDF. È possibile utilizzare anche altri formati diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

**Il file sorgente.**

![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_1.png)

Per esportare VSD diagram in PDF:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save delle classi Diagram e imposta il formato di output su PDF.

Di seguito è riportata un'immagine del file PDF di output.

**Il file PDF di output.**

![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_2.png)
### **Esempio di programmazione dell'esportazione in PDF**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToPDF-ExportToPDF.java" >}}
### **Dividi più pagine**
Aspose.Diagram for Java consente di dividere più pagine durante la conversione di Microsoft Visio Diagram in PDF. Il seguente frammento di codice mostra la funzionalità.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.java" >}}
### **Usa pagina salva richiamata**
Nel caso in cui si disponga di più pagine, Aspose.Diagram for Java consente di utilizzare la richiamata per il salvataggio della pagina durante la conversione di Microsoft Visio Diagram in PDF. Il seguente frammento di codice mostra la funzionalità.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-1.java" >}}

#### **Classe TestDiagramPageSavingCallback**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-DiagramConversions-DocumentConversionProgress-2.java" >}}
