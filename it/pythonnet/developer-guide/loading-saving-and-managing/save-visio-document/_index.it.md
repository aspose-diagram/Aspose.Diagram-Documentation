---
title: Salva il documento Visio a livello di codice
linktitle: Salva documento Visio
type: docs
weight: 30
url: /it/python-net/save-visio-document/
description: Questa pagina descrive come salvare il documento Visio su file, eseguire lo streaming con la libreria Aspose.Diagram.
---
## **Visio Riepilogo salvataggio disegno**
 Utilizzare il[Diagram.Save]() metodo per salvare un disegno Microsoft Visio. Esistono sovraccarichi che consentono di salvare un disegno su file. Il disegno può essere salvato in qualsiasi formato di salvataggio supportato da Aspose.Diagram. Per l'elenco di tutti i formati di salvataggio supportati vedere il[SalvaFileFormat]()Enum.
## **Risparmio Visio Diagram**
 La classe Diagram di Aspose.Diagram API rappresenta un disegno Visio e gli sviluppatori possono salvare il suo oggetto Visio diagram in qualsiasi formato di file supportato. Per salvare un file Microsoft Visio, usa semplicemente il[Diagram.Save]()metodo, accetta un nome file con un percorso completo o un oggetto flusso di file. Aspose.Diagram API deduce il formato di salvataggio dall'estensione del file e offre anche un parametro aggiuntivo SaveFileFormat per specificare il formato del file di output.
### **Salva un Visio Diagram in qualsiasi formato di file supportato**
Utilizzando Aspose.Diagram API, gli sviluppatori possono salvare un Visio diagram in qualsiasi formato di file supportato come elencato di seguito:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Salvataggio Diagram Esempio di programmazione**
L'esempio seguente salva un documento in un file.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Specificando Visio Salva opzioni**
 Ce ne sono diversi[Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Salva opzioni**
Questi esempi mostrano come:

- [Utilizzare Diagram Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilizzare PDF Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilizzare HTML Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio delle immagini](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilizzare SVG Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Utilizzare SWF Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Uso delle opzioni di salvataggio Diagram**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato Visio.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **Uso delle opzioni di salvataggio PDF**
The code below shows how to set save options before saving a document to a PDF format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.PdfSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the pdf format
diagram.save("CreateNewVisio_out.pdf", options)
{{< /highlight >}}




#### **Uso delle opzioni di salvataggio HTML**
The code below shows how to set save options before saving a document to HTML file format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.HTMLSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the html format
diagram.save("Visio_out.html", options)
{{< /highlight >}}




#### **Utilizzo delle opzioni di salvataggio delle immagini**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato file immagine.




{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}



Uso delle opzioni di salvataggio SVG

Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato SVG.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as svg
options = saving.SVGSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the svg format
diagram.save("ExportPageToSvg_out.svg", options)
{{< /highlight >}}


Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

### ` `**Saving VSD File to Other Formats with Aspose.Diagram for Python via .NET**
Utilizzando Aspose.Diagram, gli sviluppatori non hanno bisogno di Microsoft Office Visio nella macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

I frammenti di codice seguenti mostrano come:

1. Carica un diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for Python via .NET Programming Sample**
{{% alert color="primary" %}} 

import aspose.diagram
da aspose.diagram importazione *

{{% /alert %}} 

**Esempio:**


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save the diagram as VDX
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToVDXwithAspose_out.vdx"), SaveFileFormat.VDX)

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToPDFwithAspose_out.pdf"), SaveFileFormat.PDF)

#// Save as JPEG
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToJPGwithAspose_out.jpg"), SaveFileFormat.JPEG)
{{< /highlight >}}

