---
title: Üçgen çiz
type: docs
weight: 60
url: /tr/net/drawing/draw-triangle
description: Bu bölüm visio numaralı sayfada Aspose.Diagram ile nasıl üçgen çizileceğini açıklar. C# kullanarak üçgen çizmeyi ve pdf, svg, html, image, xps ve diğer formatlarda kaydetmeyi destekler.
---
## **Visio'de Üçgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada üçgen şekli çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde nasıl üçgen çizileceğini gösterir.


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


## **SVG'de Üçgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir üçgen çizip SVG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir üçgenin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.


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


## **PDF'de Üçgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir üçgen çizip PDF formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir üçgenin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.


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


## **PNG'de Üçgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir üçgen çizip PNG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir üçgenin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.


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


## **HTML'de Üçgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir üçgen çizip HTML formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir üçgenin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.


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

