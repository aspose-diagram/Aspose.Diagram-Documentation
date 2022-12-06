---
title: Impostare l'orientamento e controllare l'esportazione delle pagine nascoste Visio al salvataggio
type: docs
weight: 20
url: /it/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Questa sezione spiega come impostare il layout della pagina con Aspose.Diagram.
---
## **Cambia un layout di pagina Visio in Verticale o Orizzontale**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API consente agli sviluppatori di impostare l'orientamento della pagina di disegno Visio a livello di codice. Questo argomento della guida spiega come eseguire questa attività.

 Aspose.Diagram for .NET API ha il[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class che rappresenta una pagina di disegno Visio. La proprietà PageSheet esposta dalla classe Page espone anche le proprietà di stampa. Il campo PrintPageOrientation delle proprietà di stampa permette di ruotare la pagina. Offre tre opzioni come Verticale, Orizzontale e come sulla stampante. Il campo PrintPageOrientation può essere impostato a livello di codice utilizzando Aspose.Diagram API.

Questo esempio funziona come segue:

1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Estrai una pagina Visio
1. Impostare il suo orientamento come Verticale, Orizzontale o uguale a quello della stampante.
1. Salva lo Visio diagram.
### **Esempio di programmazione dell'orientamento impostato**
L'esempio di codice seguente mostra come impostare l'orientamento della pagina Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-SetVisioPageOrientation-SetVisioPageOrientation.cs" >}}
## **Controlla l'esportazione di pagine nascoste Visio al salvataggio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)API consente agli sviluppatori di includere o escludere pagine Visio nascoste salvando diagram in file PDF, HTML, immagine (PNG, JPEG, GIF), SVG e XPS. Anche loro possono nascondere Visio pagine utilizzando Aspose.Diagram API perché la sua opzione è già disponibile tramite la cella UIVisibility nella pagina ShapeSheet.
### **Nascondi una pagina nel Visio Diagram e imposta l'opzione di esportazione**
 Aspose.Diagram for .NET API ha il[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class che rappresenta una pagina di disegno Visio. La proprietà PageSheet esposta dalla classe Page espone anche le proprietà della pagina. Il campo UIVisibility delle proprietà della pagina consente di nascondere la pagina. Gli sviluppatori possono quindi utilizzare la proprietà ExportHiddenPage che viene aggiunta nelle classi SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions e PdfSaveOptions.
#### **Impostare l'opzione di esportazione per PDF**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato PDF.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToPDF-ExportOfHiddenVisioPagesToPDF.cs" >}}
#### **Impostare l'opzione di esportazione per HTML**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato HTML.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToHTML-ExportOfHiddenVisioPagesToHTML.cs" >}}
#### **Impostare l'opzione di esportazione per l'immagine**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato immagine.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.cs" >}}
#### **Impostare l'opzione di esportazione per SVG**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato SVG.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.cs" >}}
#### **Impostare l'opzione di esportazione per XPS**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram nel formato XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-ExportOfHiddenVisioPagesToXPS-ExportOfHiddenVisioPagesToXPS.cs" >}}
