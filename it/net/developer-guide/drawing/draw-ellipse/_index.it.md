---
title: Disegna Ellisse
type: docs
weight: 20
url: /it/net/drawing/draw-ellipse
description: Questa sezione spiega come disegnare un'ellisse, un cerchio o un ovale in una pagina visio con Aspose.Diagram. Supporta l'utilizzo di C# per disegnare un cerchio o un ovale e salvare come pdf, svg, html, immagine, xps e altri formati.
---
## **Disegna un cerchio in Visio**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma circolare in una pagina. L'esempio di codice seguente mostra come disegnare un cerchio in un disegno Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Disegna un cerchio in SVG**
Aspose.Diagram for .NET API allows developers to draw a circle in the page and save as SVG format. The code example below shows how to draw a circle in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram as SVG images
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.SVG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Disegna un cerchio in PDF**
Aspose.Diagram for .NET API allows developers to draw a circle in the page and save as PDF format. The code example below shows how to draw a circle in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Disegna un cerchio in PNG**
Aspose.Diagram for .NET API allows developers to draw a circle in the page and save as PNG format. The code example below shows how to draw a circle in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Disegna un cerchio in HTML**
Aspose.Diagram for .NET API allows developers to draw a circle in the page and save as HTML format. The code example below shows how to draw a circle in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 1, 2, 2);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}


## **Disegna Oval in Visio**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma ovale in una pagina. L'esempio di codice seguente mostra come disegnare un ovale in un disegno Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Disegna Oval in SVG**
Aspose.Diagram for .NET API allows developers to draw a oval in the page and save as SVG format. The code example below shows how to draw a oval in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram as SVG images
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.SVG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Disegna Oval in PDF**
Aspose.Diagram for .NET API allows developers to draw a oval in the page and save as PDF format. The code example below shows how to draw a oval in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Disegna Oval in PNG**
Aspose.Diagram for .NET API allows developers to draw a oval in the page and save as PNG format. The code example below shows how to draw a oval in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawEllipseInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Disegna Oval in HTML**
Aspose.Diagram for .NET API allows developers to draw a oval in the page and save as HTML format. The code example below shows how to draw a oval in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw ellipse in diagram
diagram.Pages[0].DrawEllipse(1, 2, 2, 4);
// Save diagram
diagram.Save(dataDir + "DrawEllipseInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}


