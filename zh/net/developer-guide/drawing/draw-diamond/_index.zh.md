---
title: 画钻石
type: docs
weight: 30
url: /zh/net/drawing/draw-diamond
description: 本节介绍如何在visio页面用Aspose.Diagram绘制菱形。支持用C#绘制菱形并保存为pdf、svg、html、image、xps等格式。
---
## **在 Visio 中绘制钻石**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制菱形。下面的代码示例显示了如何在 Visio 绘图中绘制菱形。


{{< highlight csharp >}}
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


## **在 SVG 中绘制钻石**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as SVG format. The code example below shows how to draw a diamond in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
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


## **在 PDF 中绘制钻石**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as PDF format. The code example below shows how to draw a diamond in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
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


## **在 PNG 中绘制钻石**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as PNG format. The code example below shows how to draw a diamond in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
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


## **在 HTML 中绘制钻石**
Aspose.Diagram for .NET API allows developers to draw a diamond in the page and save as HTML format. The code example below shows how to draw a diamond in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
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

