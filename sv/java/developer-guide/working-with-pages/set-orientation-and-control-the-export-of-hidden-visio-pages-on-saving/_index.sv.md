---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/java/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
---
## **Ändra en Visio sidlayout till stående eller liggande**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API tillåter utvecklare att ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for Java API har[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet PrintPageOrientation i utskriftsegenskaperna gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.
### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.


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

## **Kontrollera exporten av dolda Visio-sidor när du sparar**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API tillåter utvecklare att inkludera eller utesluta dolda Visio sidor när de sparar diagram till PDF, HTML, bild (PNG, JPEG, GIF), 3416, 34716 och 34716 och 34716 Även de kan dölja Visio sidor med Aspose.Diagram API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility på sidan ShapeSheet.
### **Göm en sida i Visio Diagram och ange exportalternativ**
 Aspose.Diagram for Java API har[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. UIVisibility-fältet i sidegenskaperna gör det möjligt att dölja sidan. Utvecklare kan sedan använda egenskapen ExportHiddenPage som läggs till i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions.
#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till PDF.


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

#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till HTML.


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

#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.


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

#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till SVG.


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

