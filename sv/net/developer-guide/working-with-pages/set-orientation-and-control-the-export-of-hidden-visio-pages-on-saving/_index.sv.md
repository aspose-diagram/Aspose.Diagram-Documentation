---
title: Ställ in orientering och kontrollera exporten av dolda Visio sidor vid sparande
type: docs
weight: 20
url: /sv/net/set-orientation-and-control-the-export-of-hidden-visio-pages-on-saving/
description: Det här avsnittet förklarar hur du ställer in sidans layout med Aspose.Diagram.
---
## **Ändra en Visio sidlayout till stående eller liggande**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API tillåter utvecklare att ställa in orienteringen för Visio ritsidan programmatiskt. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for .NET API har[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också utskriftsegenskaperna. Fältet PrintPageOrientation i utskriftsegenskaperna gör det möjligt att rotera sidan. Den erbjuder tre alternativ som stående, liggande och samma som på skrivaren. Fältet PrintPageOrientation kan ställas in programmatiskt med Aspose.Diagram API.

Detta exempel fungerar enligt följande:

1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Extrahera en Visio sida
1. Ställ in orienteringen som Stående, Liggande eller samma som på skrivaren.
1. Spara Visio diagram.
### **Ställ in orienteringsprogrammeringsexempel**
Kodexemplet nedan visar hur du ställer in orienteringen för sidan Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Flow 1");
// Page orientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;
// Save Visio
diagram.Save(dataDir + "SetPageOrientation_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Kontrollera exporten av dolda Visio-sidor när du sparar**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API tillåter utvecklare att inkludera eller utesluta dolda Visio sidor när de sparar diagram till PDF, HTML, bild (PNG, JPEG, GIF), 3416, 34716 och 34716 och 34716 Även de kan dölja Visio sidor med Aspose.Diagram API eftersom dess alternativ redan är tillgängligt via cellen UIVisibility på sidan ShapeSheet.
### **Göm en sida i Visio Diagram och ange exportalternativ**
 Aspose.Diagram for .NET API har[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass som representerar en Visio ritsida. Egenskapen PageSheet som exponeras av klassen Page exponerar också sidegenskaperna. UIVisibility-fältet i sidegenskaperna gör det möjligt att dölja sidan. Utvecklare kan sedan använda egenskapen ExportHiddenPage som läggs till i klasserna SVGSaveOptions, XPSSaveOptions, ImageSaveOptions, HTMLSaveOptions och PdfSaveOptions.
#### **Ställ in exportalternativet för PDF**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
PdfSaveOptions options = new PdfSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToPDF_out.pdf", options);

{{< /highlight >}}
```
#### **Ställ in exportalternativet för HTML**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till HTML.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToHTML_out.html", options);

{{< /highlight >}}
```
#### **Ställ in exportalternativet för bild**
Koden nedan visar hur du ställer in sparalternativ innan du sparar ett diagram till bildformat.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
ImageSaveOptions options = new ImageSaveOptions(SaveFileFormat.JPEG);
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export option of comments
options.IsExportComments = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToImage_out.jpeg", options);

{{< /highlight >}}
```
#### **Ställ in exportalternativet för SVG**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till SVG.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = UIVisibilityValue.Visible;

// Initialize PDF save options
SVGSaveOptions options = new SVGSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;
// Set export guide shapes 
options.ExportGuideShapes = false;
// Set save format
options.SaveFormat = Aspose.Diagram.SaveFileFormat.SVG;
// Set SVG fit to view port
options.SVGFitToViewPort = true;
// Set export element as Rectangle
options.ExportElementAsRectTag = true;


// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToSVG_out.svg", options);

{{< /highlight >}}
```
#### **Ställ in exportalternativet för XPS**
Koden nedan visar hur du ställer in sparalternativ innan du sparar formatet diagram till XPS.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a particular page
Page page = diagram.Pages.GetPage("Flow 2");
// Set Visio page visiblity
page.PageSheet.PageProps.UIVisibility.Value = BOOL.True;

// Initialize PDF save options
XPSSaveOptions options = new XPSSaveOptions();
// Set export option of hidden Visio pages
options.ExportHiddenPage = false;

// Save the Visio diagram
diagram.Save(dataDir + "ExportOfHiddenVisioPagesToXPS_out.xps", options);

{{< /highlight >}}
```
