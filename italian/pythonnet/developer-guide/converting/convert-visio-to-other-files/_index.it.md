---
title:  Converti Visio in altri formati
linktitle:  Converti Visio in altri formati
type: docs
weight: 40
url: /it/python-net/convert-visio-to-other-files/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio nei formati SVG, XPS, XML, XAML. Converti VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in SVG, XPS, XML, XAML con poche righe di codice.
---
## **Esporta in XML**
### **Esporta Microsoft Visio Disegno in PDF**
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in PDF utilizzando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToPdf.py" >}}

 Questo articolo spiega come esportare un Microsoft Visio diagram in XML utilizzando[Aspose.Diagram per Python tramite .NET](https://products.aspose.com/diagram/python-net/) API.

- VDX definisce un XML diagram.
- VTX definisce un modello XML.
- VSX definisce uno stencil XML.

 I costruttori della classe [Diagram] leggono un diagram e il metodo Save viene utilizzato per salvare o esportare un diagram in un formato di file diverso. I frammenti di codice in questo articolo mostrano come utilizzare il metodo Save per salvare un file Visio in[VDX](https://docs.aspose.com/diagram/python-net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/python-net/save-visio-document/) e[VSX](https://docs.aspose.com/diagram/python-net/save-visio-document/).

L'immagine seguente mostra lo diagram che viene esportato nei frammenti di codice seguenti. Il file esportato viene mostrato prima di ogni frammento di codice.

|**A Microsoft Visio diagram in procinto di essere esportato.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_3.png)|

### **Esporta da VSD a VDX**
VDX è un formato di file XML basato su schema che consente di salvare i diagrammi in un formato leggibile da prodotti diversi da Microsoft Visio. È un formato utile per trasferire diagrammi tra applicazioni software e conservare dati modificabili.

Per esportare un VSD da diagram a VDX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VDX.

|**Il file VDX esportato.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_4.png)|

### **Esporta da VSD a VSX**
VSX è un formato XML per definire gli stencil, gli oggetti di base da cui viene creato un diagram. Quando un file Visio viene convertito in VSX, vengono esportati solo gli stencil.

Per esportare un VSD da diagram a VSX:

- Creare un'istanza della classe Diagram.
- Chiamare il metodo Save della classe Diagram per scrivere il file di disegno Visio in VSX.
### **Esporta da VSD a VTX**
TVX è una rappresentazione XML di un file modello e memorizza le impostazioni per il documento.

Per esportare un VSD da diagram a VTX:

1. Creare un'istanza della classe Diagram.
1. Chiamare il metodo Save della classe diagram per scrivere il file di disegno Visio nel formato VTX.
### **Esporta Microsoft Visio Disegno in XML**
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in XML utilizzando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXml.py" >}}

## **Esporta in XPS**
 Questo articolo spiega come esportare un Microsoft Visio diagram in XPS utilizzando[Aspose.Diagram per Python tramite .NET](https://products.aspose.com/diagram/python-net/) API.
Utilizzare il costruttore [Diagram]class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

I frammenti di codice in questo articolo accettano come input lo diagram riportato di seguito. Puoi utilizzare anche altri formati diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX o VSX).

|**Il documento di origine.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_5.png)|


Per esportare VSD diagram in XPS:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save della classe Diagram e imposta XPS come formato di output.
### **Esporta Microsoft Visio Disegno in XPS**
Gli esempi di codice mostrano come esportare il disegno Microsoft Visio in XPS utilizzando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToXps.py" >}}

## **Esporta un Diagram in SVG**
Questo articolo spiega come esportare un Microsoft Visio diagram in SVG (Scalable Vector Graphics) utilizzando[Aspose.Diagram per Python tramite .NET](https://products.aspose.com/diagram/python-net/) API.

Utilizzare il costruttore [Diagram]class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

Per esportare VSD diagram in SVG, attenersi alla seguente procedura:

1. Creare un'istanza della classe Diagram.
1. Chiama il metodo Save della classe e imposta SVG come formato di esportazione.
### **Esporta Microsoft Visio Disegno in SVG**
Gli esempi di codice mostrano come esportare un diagram in SVG utilizzando C#.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-ExportToSvg.py" >}}

Per esportare un disegno Visio con forme selettive:

1. Creare un'istanza della classe Diagram.
1. Crea un'istanza di qualsiasi classe SaveOption per specificare le impostazioni come descritto qui:[Specificare Visio Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Chiamare il metodo Save dell'oggetto di classe Diagram e passare l'oggetto di classe dell'opzione di salvataggio come parametro.
### **Conversione Visio Disegno con esempio di programmazione di forme selettive**
L'esempio di codice mostra come esportare un disegno con forme Visio selettive.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-PythonNet-ConvertVisioWithSelectiveShapes.py" >}}