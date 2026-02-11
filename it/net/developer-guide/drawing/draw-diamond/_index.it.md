---
title: Disegna diamante
type: docs
weight: 30
url: /it/net/drawing/draw-diamond
description: Questa sezione spiega come disegnare un diamante in una pagina visio con Aspose.Diagram. Supporta l'utilizzo di C# per disegnare un diamante e salvarlo come pdf, svg, html, immagine, xps e altri formati.
---
## **Disegna Diamante in Visio**
Aspose.Diagram for .NET API consente agli sviluppatori di disegnare una forma a diamante in una pagina. L'esempio di codice seguente mostra come disegnare un diamante in un disegno Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Disegna Diamante in SVG**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as SVG format. The code example below shows how to draw a diamond in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawDiamondInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Disegna Diamante in PDF**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as PDF format. The code example below shows how to draw a diamond in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Disegna Diamante in PNG**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as PNG format. The code example below shows how to draw a diamond in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawDiamondInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Disegna Diamante in HTML**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as HTML format. The code example below shows how to draw a diamond in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 2), new PointF(2, 0), new PointF(3, 2), new PointF(2, 4), new PointF(1, 2) };
//Draw Diamond in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawDiamondInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

