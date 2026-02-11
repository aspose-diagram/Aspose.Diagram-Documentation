---
title: Quadrat zeichnen
type: docs
weight: 50
url: /de/net/drawing/draw-square
description: In diesem Abschnitt wird erklärt, wie man ein Quadrat auf einer visio-Seite mit Aspose.Diagram zeichnet. Unterstützung bei der Verwendung von C# zum Zeichnen von Quadraten und zum Speichern als PDF, SVG, HTML, Bild, XPS und andere Formate.
---
## **Zeichnen Sie ein Quadrat in Visio**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, eine quadratische Form auf einer Seite zu zeichnen. Das folgende Codebeispiel zeigt, wie ein Quadrat in einer Visio-Zeichnung gezeichnet wird.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Zeichnen Sie ein Quadrat in SVG**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as SVG format. The code example below shows how to draw a square in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawSquareInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Zeichnen Sie ein Quadrat in PDF**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as PDF format. The code example below shows how to draw a square in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Zeichnen Sie ein Quadrat in PNG**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as PNG format. The code example below shows how to draw a square in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawSquareInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Zeichnen Sie ein Quadrat in HTML**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as HTML format. The code example below shows how to draw a square in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw square in page
diagram.Pages[0].DrawRectangle(1, 1, 2, 2);

// Save diagram
diagram.Save(dataDir + "DrawSquareInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

