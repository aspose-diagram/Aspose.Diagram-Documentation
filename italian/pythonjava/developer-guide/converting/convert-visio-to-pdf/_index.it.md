---
title:  Converti Visio in formato PDF
linktitle: Converti Visio in PDF
type: docs
weight: 10
url: /it/python-java/convert-visio-to-pdf/
description: This topic show you how to convert Visio to PDF formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PDF with a few lines of code.
---
## **Esportazione in PDF**
{{% alert color="primary" %}}

Aspose.Diagram per Python tramite Java scrive direttamente le informazioni su API e il numero di versione nei documenti di output. Ad esempio, dopo il rendering di un disegno in PDF, Aspose.Diagram for Java viene popolato**Applicazione**campo con valore 'Aspose.Diagram' e**Produttore PDF**campo con un valore, ad esempio 'Aspose.Diagram 17.9'.

Si prega di notare che non è possibile istruire Aspose.Diagram per Python tramite Java per modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

Questo articolo spiega come esportare un Microsoft Visio diagram in PDF utilizzando Aspose.Diagram per Python tramite Java.

Usare il costruttore Diagram class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

[Il VSD diagram](ExportToPDF.vsd) è il file di disegno di esempio per esportare PDF. È possibile utilizzare anche altri formati diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

Per esportare VSD diagram in PDF:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save delle classi Diagram e imposta il formato di output su PDF.

### **Esempio di programmazione dell'esportazione in PDF**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToPDF.py" >}}

### **Dividi più pagine**
Aspose.Diagram for Java consente di dividere più pagine durante la conversione di Microsoft Visio Diagram in PDF. Il seguente frammento di codice mostra la funzionalità.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.py" >}}
