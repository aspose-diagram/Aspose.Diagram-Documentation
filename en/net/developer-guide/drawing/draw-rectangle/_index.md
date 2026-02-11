---
title: Draw Rectangle
type: docs
weight: 10
url: /net/drawing/draw-rectangle
description: This section explains how to draw rectangle in a visio page with Aspose.Diagram. Support using C# to draw rectangle and save as pdf, svg, html, image, xps and other formats.
---

## **Draw Rectangle in Visio**
Aspose.Diagram for .NET API allows developers to draw a rectangle shape in a page.The code example below shows how to draw a rectangle in a Visio drawing.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Draw Rectangle in SVG**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as SVG format. The code example below shows how to draw a rectangle in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawRectangleInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Draw Rectangle in PDF**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as PDF format. The code example below shows how to draw a rectangle in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Draw Rectangle in PNG**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as PNG format. The code example below shows how to draw a rectangle in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawRectangleInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Draw Rectangle in HTML**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as HTML format. The code example below shows how to draw a rectangle in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Draw Rectangle in page
diagram.Pages[0].DrawRectangle(1, 2, 2, 4);

// Save diagram
diagram.Save(dataDir + "DrawRectangleInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

