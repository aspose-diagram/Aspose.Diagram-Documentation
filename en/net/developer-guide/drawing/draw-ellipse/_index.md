---
title: Draw Ellipse
type: docs
weight: 20
url: /net/drawing/draw-ellipse
description: This section explains how to draw ellipse,circle or oval in a visio page with Aspose.Diagram. Support using C# to draw circle or oval and save as pdf, svg, html, image, xps and other formats.
---

## **Draw Circle in Visio**
Aspose.Diagram for .NET API allows developers to draw a circle shape in a page.The code example below shows how to draw a circle in a Visio drawing.


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


## **Draw Circle in SVG**
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


## **Draw Circle in PDF**
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


## **Draw Circle in PNG**
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


## **Draw Circle in HTML**
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


## **Draw Oval in Visio**
Aspose.Diagram for .NET API allows developers to draw a oval shape in a page.The code example below shows how to draw a oval in a Visio drawing.


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


## **Draw Oval in SVG**
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


## **Draw Oval in PDF**
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


## **Draw Oval in PNG**
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


## **Draw Oval in HTML**
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


