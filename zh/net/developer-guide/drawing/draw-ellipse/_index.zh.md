---
title: 绘制椭圆
type: docs
weight: 20
url: /zh/net/drawing/draw-ellipse
description: 本节介绍如何使用Aspose.Diagram在visio页面中绘制椭圆、圆形或椭圆。支持使用C#绘制圆形或椭圆并保存为pdf、svg、html、image、xps等格式。
---
## **在 Visio 中画圆**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制圆形。下面的代码示例显示了如何在 Visio 绘图中绘制圆形。


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


## **在 SVG 中画圆**
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


## **在 PDF 中画圆**
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


## **在 PNG 中画圆**
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


## **在 HTML 中画圆**
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


## **在 Visio 中绘制椭圆**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制椭圆形。下面的代码示例显示了如何在 Visio 绘图中绘制椭圆形。


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


## **在 SVG 中绘制椭圆**
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


## **在 PDF 中绘制椭圆**
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


## **在 PNG 中绘制椭圆**
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


## **在 HTML 中绘制椭圆**
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


