---
title: kare çiz
type: docs
weight: 50
url: /tr/net/drawing/draw-square
description: Bu bölümde visio sayfasında Aspose.Diagram ile nasıl kare çizileceği anlatılmaktadır. Kare çizmek ve pdf, svg, html, resim, xps ve diğer formatlarda kaydetmek için C#'i kullanarak destekleyin.
---
## **Visio de Kare Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada kare şekli çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde nasıl kare çizileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **SVG de Kare Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada bir kare çizip SVG formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir karenin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PDF de Kare Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada bir kare çizip PDF formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir karenin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PNG de Kare Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada bir kare çizip PNG formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir karenin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **HTML de Kare Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada bir kare çizip HTML formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir karenin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```
