---
title: Salva il documento Visio a livello di codice
linktitle: Salva documento Visio
type: docs
weight: 30
url: /it/java/save-visio-document/
description: Questa pagina descrive come salvare il documento Visio su file, eseguire lo streaming con la libreria Aspose.Diagram.
---
## **Visio Riepilogo salvataggio disegno**
 Utilizzare il[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\) per salvare un disegno Microsoft Visio. Esistono sovraccarichi che consentono di salvare un disegno su file. Il disegno può essere salvato in qualsiasi formato di salvataggio supportato da Aspose.Diagram. Per l'elenco di tutti i formati di salvataggio supportati vedere il[SalvaFileFormat](https://reference.aspose.com/diagram/java/com.aspose.diagram/SaveFileFormat)Enum.
## **Risparmio Visio Diagram**
 La classe Diagram di Aspose.Diagram API rappresenta un disegno Visio e gli sviluppatori possono salvare il suo oggetto Visio diagram in qualsiasi formato di file supportato. Per salvare un file Microsoft Visio, usa semplicemente il[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)), accetta un nome file con il percorso completo o un oggetto flusso di file. Aspose.Diagram API deduce il formato di salvataggio dall'estensione del file e offre anche un parametro SaveFileFormat aggiuntivo per specificare il formato del file di output.
### **Salva un Visio Diagram in qualsiasi formato di file supportato**
Utilizzando Aspose.Diagram API, gli sviluppatori possono salvare un Visio diagram in qualsiasi formato di file supportato come elencato di seguito:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG and XAML**
### **Salvataggio Diagram Esempio di programmazione**
L'esempio seguente salva un documento in un file.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-SaveVisioDiagram-SaveVisioDiagram.java" >}}
## **Specificando Visio Salva opzioni**
 Ce ne sono diversi[Diagram.Save](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram#save\(java.lang.String,%20int\)) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Salva opzioni**
Questi esempi mostrano come:

- [Utilizzare Diagram Opzioni di salvataggio](/diagram/it/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilizzare PDF Opzioni di salvataggio](/diagram/it/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilizzare HTML Opzioni di salvataggio](/diagram/it/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Usa le opzioni di salvataggio delle immagini](/diagram/it/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
- [Utilizzare SVG Opzioni di salvataggio](/diagram/it/java/save-a-visio-drawing-to-pdf-2c-html-and-other-formats/).
#### **Uso delle opzioni di salvataggio Diagram**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseDiagramSaveOptions-UseDiagramSaveOptions.java" >}}



#### **Uso delle opzioni di salvataggio PDF**
The code below shows how to set save options before saving a document to a PDF format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UsePDFSaveOptions-UsePDFSaveOptions.java" >}}



#### **Uso delle opzioni di salvataggio HTML**
The code below shows how to set save options before saving a document to a HTML format.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseHTMLSaveOptions-UseHTMLSaveOptions.java" >}}



#### **Utilizzo delle opzioni di salvataggio delle immagini**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in un formato immagine.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseImageSaveOptions-UseImageSaveOptions.java" >}}
#### **Uso delle opzioni di salvataggio SVG**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento nel formato SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-VisioSaveOptions-UseSVGSaveOptions-UseSVGSaveOptions.java" >}}
