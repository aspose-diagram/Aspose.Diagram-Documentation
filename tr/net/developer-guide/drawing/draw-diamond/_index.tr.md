---
title: Elmas çiz
type: docs
weight: 30
url: /tr/net/drawing/draw-diamond
description: Bu bölüm visio sayfasında Aspose.Diagram ile nasıl elmas çizileceğini açıklar. Elmas çizmek ve pdf, svg, html, image, xps ve diğer formatlarda kaydetmek için C# kullanarak destekleyin.
---
## **Visio'de Elmas Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada baklava şekli çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde elmasın nasıl çizileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **SVG'de Elmas Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir elmas çizmesine ve SVG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir elmasın nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PDF'de Elmas Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir elmas çizmesine ve PDF formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir elmasın nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PNG'de Elmas Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir elmas çizmesine ve PNG formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir elmasın nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **HTML'de Elmas Çiz**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir elmas çizmesine ve HTML formatında kaydetmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde bir elmasın nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```
