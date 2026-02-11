---
title: Rita triangel
type: docs
weight: 60
url: /sv/net/drawing/draw-triangle
description: Det här avsnittet förklarar hur man ritar triangel på en visio-sida med Aspose.Diagram. Stöd att använda C# för att rita triangel och spara som pdf, svg, html, bild, xps och andra format.
---
## **Rita triangeln i Visio**
Aspose.Diagram for .NET API tillåter utvecklare att rita en triangelform på en sida. Kodexemplet nedan visar hur man ritar en triangel i en Visio-ritning.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Rita triangeln i SVG**
Aspose.Diagram for .NET API låter utvecklare rita en triangel på sidan och spara som SVG-format. Kodexemplet nedan visar hur man ritar en triangel i en Visio-ritning och sparar som SVG-format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawTriangleInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **Rita triangeln i PDF**
Aspose.Diagram for .NET API låter utvecklare rita en triangel på sidan och spara som PDF-format. Kodexemplet nedan visar hur man ritar en triangel i en Visio-ritning och sparar som PDF-format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **Rita triangeln i PNG**
Aspose.Diagram for .NET API låter utvecklare rita en triangel på sidan och spara som PNG-format. Kodexemplet nedan visar hur man ritar en triangel i en Visio-ritning och sparar som PNG-format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawTriangleInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **Rita triangeln i HTML**
Aspose.Diagram for .NET API låter utvecklare rita en triangel på sidan och spara som HTML-format. Kodexemplet nedan visar hur man ritar en triangel i en Visio-ritning och sparar som HTML-format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(5, 1), new PointF(3, 4.464f), new PointF(1, 1) };
//Draw Triangle in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawTriangleInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

