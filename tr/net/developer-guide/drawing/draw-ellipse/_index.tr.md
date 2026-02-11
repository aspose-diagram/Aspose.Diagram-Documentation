---
title: Elips Çiz
type: docs
weight: 20
url: /tr/net/drawing/draw-ellipse
description: Bu bölüm visio numaralı sayfada Aspose.Diagram ile elips, daire veya ovalin nasıl çizileceğini açıklar. Daire veya oval çizmek ve pdf, svg, html, resim, xps ve diğer formatlarda kaydetmek için C#'i kullanarak destekleyin.
---
## **Visio'de Daire Çiz**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada daire şekli çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde nasıl daire çizileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **SVG'de Daire Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada daire çizip SVG formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir dairenin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PDF'de Daire Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada daire çizip PDF formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir dairenin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PNG'de Daire Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada daire çizip PNG formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir dairenin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **HTML'de Daire Çiz**
Aspose.Diagram for .NET API geliştiricilerin sayfada daire çizip HTML formatında kaydetmesine olanak sağlar. Aşağıdaki kod örneği, Visio çiziminde bir dairenin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **Visio'de Oval çizin**
Aspose.Diagram for .NET API, geliştiricilerin bir sayfada oval bir şekil çizmesine olanak tanır. Aşağıdaki kod örneği, Visio çiziminde nasıl oval çizileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **SVG'de Oval çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir oval çizip SVG formatında kaydetmelerini sağlar. Aşağıdaki kod örneği, Visio çiziminde bir ovalin nasıl çizileceğini ve SVG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PDF'de Oval çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir oval çizip PDF formatında kaydetmelerini sağlar. Aşağıdaki kod örneği, Visio çiziminde bir ovalin nasıl çizileceğini ve PDF formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **PNG'de Oval çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir oval çizip PNG formatında kaydetmelerini sağlar. Aşağıdaki kod örneği, Visio çiziminde bir ovalin nasıl çizileceğini ve PNG formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

## **HTML'de Oval çizin**
Aspose.Diagram for .NET API, geliştiricilerin sayfada bir oval çizip HTML formatında kaydetmelerini sağlar. Aşağıdaki kod örneği, Visio çiziminde bir ovalin nasıl çizileceğini ve HTML formatında nasıl kaydedileceğini gösterir.

```
{{< highlight "csharp" >}}
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
```

