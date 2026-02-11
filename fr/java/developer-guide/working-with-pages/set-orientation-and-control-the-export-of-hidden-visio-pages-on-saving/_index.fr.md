---
title: Définir l'orientation et contrôler l'exportation des pages masquées Visio lors de l'enregistrement
type: docs
weight: 20
url: /fr/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Changer une mise en page Visio en portrait ou paysage**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API permet aux développeurs de définir l'orientation de la page de dessin Visio par programmation. Cette rubrique d'aide explique comment accomplir cette tâche.

 Aspose.Diagram for Java API a le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés d'impression. Le champ PrintPageOrientation des propriétés d'impression permet de faire pivoter la page. Il offre trois options : Portrait, Paysage et même que sur l'imprimante. Le champ PrintPageOrientation peut être défini par programmation à l'aide de Aspose.Diagram API.

Cet exemple fonctionne comme suit :

1. Chargez un Visio diagram existant dans l'objet de classe Diagram.
1. Extraire une page Visio
1. Définissez son orientation sur Portrait, Paysage ou identique à celle de l'imprimante.
1. Enregistrez le Visio diagram.
### **Définir l'exemple de programmation d'orientation**
L'exemple de code ci-dessous montre comment définir l'orientation de la page Visio.


{{< highlight java >}}
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

## **Contrôler l'exportation des pages masquées Visio lors de l'enregistrement**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API allows developers to include or exclude hidden Visio pages on saving diagram to PDF, HTML, Image (PNG, JPEG, GIF), SVG, and XPS files. Even they may hide Visio pages using Aspose.Diagram API because its option is already available through the cell UIVisibility in the page ShapeSheet.
### **Masquer une page dans le Visio Diagram et définir l'option d'exportation**
 Aspose.Diagram for Java API a le[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) classe qui représente une page de dessin Visio. La propriété PageSheet exposée par la classe Page expose également les propriétés de la page. Le champ UIVisibility des propriétés de la page permet de masquer la page. Les développeurs peuvent ensuite utiliser la propriété ExportHiddenPage qui est ajoutée dans les classes SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions et PdfSaveOptions.
#### **Set the Export Option for PDF**
The code below shows how to set save options before saving a diagram to PDF format.


{{< highlight java >}}
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

#### **Set the Export Option for HTML**
The code below shows how to set save options before saving a diagram to HTML format.


{{< highlight java >}}
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

#### **Définir l'option d'exportation pour l'image**
Le code ci-dessous montre comment définir les options d'enregistrement avant d'enregistrer un diagram au format image.


{{< highlight java >}}
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

#### **Set the Export Option for SVG**
The code below shows how to set save options before saving a diagram to SVG format.


{{< highlight java >}}
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

