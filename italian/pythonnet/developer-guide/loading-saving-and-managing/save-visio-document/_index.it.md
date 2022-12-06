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
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG e SWF**
### **Salvataggio Diagram Esempio di programmazione**
L'esempio seguente salva un documento in un file.

{{< highlight "java" >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Specificando Visio Salva opzioni**
 Ce ne sono diversi[Diagram.Save]() overload del metodo che accettano un oggetto SaveOptions. Dovrebbe essere un oggetto di una classe derivata dalla classe SaveOptions. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio. Ad esempio, esiste PdfSaveOptions per il formato di salvataggio SaveFileFormat.PDF.
### **Visio Diagram Salva opzioni**
Questi esempi mostrano come:

- [Utilizzare Diagram Opzioni di salvataggio](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio PDF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio HTML](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio delle immagini](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio SVG](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Usa le opzioni di salvataggio SWF](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Uso delle opzioni di salvataggio Diagram**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato Visio.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseDiagramSaveOptions.py" >}}



#### **Uso delle opzioni di salvataggio PDF**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato PDF.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UsePdfSaveOptions.py" >}}



#### **Uso delle opzioni di salvataggio HTML**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato file HTML.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseHtmlSaveOptions.py" >}}



#### **Utilizzo delle opzioni di salvataggio delle immagini**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato file immagine.



{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseImageSaveOptions.py" >}}


Uso delle opzioni di salvataggio SVG

Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato SVG.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-UseSvgSaveOptions.py" >}}

A volte, gli sviluppatori devono salvare o esportare i diagrammi Visio in diversi formati di file in modo programmatico (come VDX, PDF, JPEG e così via).

### ` `**Salvataggio del file VSD in altri formati con Aspose.Diagram per Python tramite .NET**
Utilizzando Aspose.Diagram, gli sviluppatori non hanno bisogno di Microsoft Office Visio nella macchina e possono lavorare indipendentemente dall'automazione Microsoft Office.

I frammenti di codice seguenti mostrano come:

1. Carica un diagram.
1. Salva lo diagram al VSX, PDF e JPEG.
#### **Salvataggio del file VSD con Aspose.Diagram per Python tramite Esempio di programmazione .NET**
{{% alert color="primary" %}} 

import aspose.diagram
da aspose.diagram importazione *

{{% /alert %}} 

**Esempio:**

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-SaveDiagramTo_VDX_PDF_JPEG_withAspose.py" >}}
