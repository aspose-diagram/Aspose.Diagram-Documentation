---
title:  Converti Visio in formato PDF
linktitle: Converti Visio in PDF
type: docs
weight: 10
url: /it/net/convert-visio-to-pdf/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in formati PDF. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in PDF con poche righe di codice.
---
## **Esporta in PDF**
{{% alert color="primary" %}}

Aspose.Diagram for .NET scrive direttamente le informazioni su API e il numero di versione nei documenti di output. Ad esempio, durante il rendering di un disegno in PDF, Aspose.Diagram for .NET viene popolato**Applicazione** campo con valore 'Aspose.Diagram' e**Produttore PDF** campo con valore, ad esempio 'Aspose.Diagram 17.9'.

Si noti che non è possibile incaricare Aspose.Diagram for .NET API di modificare o rimuovere queste informazioni dai documenti di output.

{{% /alert %}}

 Questo articolo spiega come esportare un Microsoft Visio diagram in PDF utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Utilizzare il[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) costruttore di classe per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

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
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in PDF utilizzando C#.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ExportToPDF-ExportToPDF.cs" >}}
### **Dividi più pagine**
Aspose.Diagram for .NET consente di dividere più pagine durante la conversione di Microsoft Visio Diagram in PDF. Il seguente frammento di codice mostra la funzionalità.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-SplitMultiPages.cs" >}}
### **Usa pagina salva richiamata**
Nel caso in cui si disponga di più pagine, Aspose.Diagram for .NET consente di utilizzare la richiamata per il salvataggio della pagina durante la conversione di Microsoft Visio Diagram in PDF. Il seguente frammento di codice mostra la funzionalità.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-VisioSaveOptions-UsePDFSaveOptions-PageSavingCallback.cs" >}}
#### **Classe TestDiagramPageSavingCallback**
{{< highlight "java" >}}

 classe pubblica TestDiagramPageSavingCallback : Aspose.Diagram.Saving.IPageSavingCallback

{  public void PageStartSaving(Aspose.Diagram.Saving.PageStartSavingArgs args)  {  Console.WriteLine("Inizia a salvare diagram pagina {0} di pagine {1}", args.PageIndex + 1, args.PageCountd_x00PageCountd);_x000PageCountd);   }  public void PageEndSaving(Aspose.Diagram.Saving.PageEndSavingArgs args)  {  Console.WriteLine("Termina salvataggio diagram pagina {0} di pagine {1}", args.PageIndex + 1,PageCount args.Page);   //non restituisce le pagine dopo l'indice di pagina 8.  if (args.PageIndex >= 8)  {  args.HasMorePages = false;  } _x0_x0d_0}
