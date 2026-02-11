---
title: Pentagon çiz
type: docs
weight: 40
url: /tr/net/drawing/draw-pentagon
description: Bu bölüm visio sayfasında Aspose.Diagram ile beşgenin nasıl çizileceğini açıklar. Beşgen çizmek ve pdf, svg, html, resim, xps ve diğer formatlarda kaydetmek için C# kullanarak destekleyin.
---
## **Visio'de Pentagon çizin**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada bir beşgen şekli çizmesine olanak tanır. Aşağıdaki kod örneği, bir Visio çiziminde bir beşgenin nasıl çizileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **SVG'de Pentagon çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir beşgen çizmesine ve SVG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir beşgenin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.svg", imageSaveOptions);

{{< /highlight >}}


## **PDF'de Pentagon çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir beşgen çizmesine ve PDF formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir beşgenin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}


## **PNG'de Pentagon çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir beşgen çizmesine ve PNG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir beşgenin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.png", imageSaveOptions);

{{< /highlight >}}


## **HTML'de Pentagon çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir beşgen çizmesine ve HTML formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir beşgenin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

