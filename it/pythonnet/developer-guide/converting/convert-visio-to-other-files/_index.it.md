---
title:  Converti Visio in altri formati
linktitle:  Converti Visio in altri formati
type: docs
weight: 40
url: /it/python-net/convert-visio-to-other-files/
description: This topic show you how to Aspose.Diagram allows to convert Visio to SVG,XPS,XML,XAML formats. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to SVG,XPS,XML,XAML with a few lines of code.
---
## **Esporta in XML**
### **Export Microsoft Visio Drawing to PDF**
The code samples show how to export Microsoft Visio Drawing to PDF using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the pdf format
diagram.save("Visio_out.pdf", SaveFileFormat.PDF)
{{< /highlight >}}


 Questo articolo spiega come esportare un Microsoft Visio diagram in XML utilizzando[Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

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


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the vdx format
diagram.save("Visio_out.vdx", SaveFileFormat.VDX)

#// Save diagram in the vtx format
diagram.save("Visio_out.vtx", SaveFileFormat.VTX)

#// Save diagram in the vsx format
diagram.save("Visio_out.vsx", SaveFileFormat.VSX)
{{< /highlight >}}


## **Export to XPS**
This article explains how to export a Microsoft Visio diagram to XPS using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.
Utilizzare il costruttore [Diagram]class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

The code snippets in this article takes the diagram below as an input. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, VTX or VSX) as well.

|**Il documento di origine.**|
|:- |
|![cose da fare:immagine_alt_testo](how-to-convert-a-visio-diagram_5.png)|


To export VSD diagram to XPS:

1. Creare un'istanza della classe Diagram.
1. Call the Diagram class' Save method and set XPS as the output format.
### **Export Microsoft Visio Drawing to XPS**
The code samples show how to export Microsoft Visio Drawing to XPS using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the xps format
diagram.save("Visio_out.xps", SaveFileFormat.XPS)
{{< /highlight >}}


## **Export a Diagram to SVG**
This article explains how to export a Microsoft Visio diagram to SVG (Scalable Vector Graphics) using [Aspose.Diagram for Python via .NET](https://products.aspose.com/diagram/python-net/) API.

Utilizzare il costruttore [Diagram]class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato.

To export VSD diagram to SVG, perform the following steps:

1. Creare un'istanza della classe Diagram.
1. Call the class' Save method and set SVG as the export format.
### **Export Microsoft Visio Drawing to SVG**
The code samples show how to export a diagram to SVG using C#.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the svg format
diagram.save("Visio_out.svg", SaveFileFormat.SVG)
{{< /highlight >}}


Per esportare un disegno Visio con forme selettive:

1. Creare un'istanza della classe Diagram.
1. Crea un'istanza di qualsiasi classe SaveOption per specificare le impostazioni come descritto qui:[Specificare Visio Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/#specifying-visio-save-options)
1. Chiamare il metodo Save dell'oggetto di classe Diagram e passare l'oggetto di classe dell'opzione di salvataggio come parametro.
### **Conversione Visio Disegno con esempio di programmazione di forme selettive**
L'esempio di codice mostra come esportare un disegno con forme Visio selettive.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.SVGSaveOptions()
shapes = options.shapes;
#// get shapes by page index and shape ID, and then add in the shape collection object
shapes.add(diagram.pages[0].shapes.get_shape(1));
shapes.add(diagram.pages[0].shapes.get_shape(2));
    
#// Save one page only, by page index
options.page_index = 0
    
#// Save resultant svg file
diagram.save("ExportToSvg_out.svg", options)
{{< /highlight >}}
