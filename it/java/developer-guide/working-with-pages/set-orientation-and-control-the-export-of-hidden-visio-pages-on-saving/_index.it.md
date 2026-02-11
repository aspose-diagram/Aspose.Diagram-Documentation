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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetVisioPageOrientation.class);  
// initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get Visio page
Page page = diagram.getPages().getPage("Flow 1");
// page orientation
page.getPageSheet().getPrintProps().getPrintPageOrientation().setValue(PrintPageOrientationValue.LANDSCAPE);
// save Visio
diagram.save(dataDir + "SetPageOrientation_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Controlla l'esportazione di pagine nascoste Visio al salvataggio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Nascondi una pagina nel Visio Diagram e imposta l'opzione di esportazione**
 Aspose.Diagram for Java API ha il[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class che rappresenta una pagina di disegno Visio. La proprietà PageSheet esposta dalla classe Page espone anche le proprietà della pagina. Il campo UIVisibility delle proprietà della pagina consente di nascondere la pagina. Gli sviluppatori possono quindi utilizzare la proprietà ExportHiddenPage che viene aggiunta nelle classi SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions e PdfSaveOptions.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ExporToHiddenVisioPagesToPdf.class);  
        
// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);

//Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToPDF_Out.pdf", options);

{{< /highlight >}}
```
#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToHtml.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}
```
#### **Impostare l'opzione di esportazione per l'immagine**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un diagram in formato immagine.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToImage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);
// initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// set export option of comments
options.setExportComments(false);

// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToImage_Out.jpeg", options);

{{< /highlight >}}
```
#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ExportOfHiddenVisioPagesToSVG.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Flow 2");
// set Visio page visiblity
page.getPageSheet().getPageProps().getUIVisibility().setValue(BOOL.TRUE);

// initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// set export option of hidden Visio pages
options.setExportHiddenPage(false);
// Set SVG fit to view port
options.setSVGFitToViewPort(true);
// Set export element as Rectangle
options.setExportElementAsRectTag(true);

// save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToSVG_Out.svg", options);

{{< /highlight >}}
```
