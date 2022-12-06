---
title: Impostare l'orientamento e controllare l'esportazione delle pagine nascoste Visio al salvataggio
type: docs
weight: 20
url: /it/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Cambia un layout di pagina Visio in Verticale o Orizzontale**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API consente agli sviluppatori di impostare l'orientamento della pagina di disegno Visio a livello di codice. Questo argomento della guida spiega come eseguire questa attività.

 Aspose.Diagram for Java API ha il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class che rappresenta una pagina di disegno Visio. La proprietà PageSheet esposta dalla classe Page espone anche le proprietà di stampa. Il campo PrintPageOrientation delle proprietà di stampa permette di ruotare la pagina. Offre tre opzioni come Verticale, Orizzontale e come sulla stampante. Il campo PrintPageOrientation può essere impostato a livello di codice utilizzando Aspose.Diagram API.

Questo esempio funziona come segue:

1. Carica un Visio diagram esistente nell'oggetto classe Diagram.
1. Estrai una pagina Visio
1. Impostare il suo orientamento come Verticale, Orizzontale o uguale a quello della stampante.
1. Salva lo Visio diagram.
### **Esempio di programmazione dell'orientamento impostato**
L'esempio di codice seguente mostra come impostare l'orientamento della pagina Visio.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-SetVisioPageOrientation-SetVisioPageOrientation.java" >}}
## **Controlla l'esportazione di pagine nascoste Visio al salvataggio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API consente agli sviluppatori di includere o escludere pagine Visio nascoste salvando diagram in file PDF, HTML, immagine (PNG, JPEG, GIF), SVG e XPS. Anche loro possono nascondere Visio pagine utilizzando Aspose.Diagram API perché la sua opzione è già disponibile tramite la cella UIVisibility nella pagina ShapeSheet.
### **Nascondi una pagina nel Visio Diagram e imposta l'opzione di esportazione**
 Aspose.Diagram for Java API ha il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class che rappresenta una pagina di disegno Visio. La proprietà PageSheet esposta dalla classe Page espone anche le proprietà della pagina. Il campo UIVisibility delle proprietà della pagina consente di nascondere la pagina. Gli sviluppatori possono quindi utilizzare la proprietà ExportHiddenPage che viene aggiunta nelle classi SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions e PdfSaveOptions.
#### **Impostare l'opzione di esportazione per PDF**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato PDF.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExporToHiddenVisioPagesToPdf-ExporToHiddenVisioPagesToPdf.java" >}}
#### **Impostare l'opzione di esportazione per HTML**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato HTML.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToHtml-ExportOfHiddenVisioPagesToHtml.java" >}}
#### **Impostare l'opzione di esportazione per l'immagine**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato immagine.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToImage-ExportOfHiddenVisioPagesToImage.java" >}}
#### **Impostare l'opzione di esportazione per SVG**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato SVG.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-ExportOfHiddenVisioPagesToSVG-ExportOfHiddenVisioPagesToSVG.java" >}}
