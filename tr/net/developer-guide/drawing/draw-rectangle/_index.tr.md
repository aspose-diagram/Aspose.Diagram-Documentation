---
title: Dikdörtgen Çiz
type: docs
weight: 10
url: /tr/net/drawing/draw-rectangle
description: Bu bölümde visio numaralı sayfada Aspose.Diagram ile nasıl dikdörtgen çizileceği anlatılmaktadır. C# ile dikdörtgen çizme ve pdf, svg, html, image, xps ve diğer formatlarda kaydetme desteği.
---
## **Visio'de Dikdörtgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada dikdörtgen şekli çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde nasıl dikdörtgen çizileceğini gösterir.


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


## **SVG'de Dikdörtgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir dikdörtgen çizip SVG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir dikdörtgenin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.


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


## **PDF'de Dikdörtgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir dikdörtgen çizip PDF formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir dikdörtgenin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.


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


## **PNG'de Dikdörtgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir dikdörtgen çizip PNG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir dikdörtgenin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.


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


## **HTML'de Dikdörtgen Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir dikdörtgen çizip HTML formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir dikdörtgenin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.


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

