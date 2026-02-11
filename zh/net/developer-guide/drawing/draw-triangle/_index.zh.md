---
title: 绘制三角形
type: docs
weight: 60
url: /zh/net/drawing/draw-triangle
description: 本节介绍如何用Aspose.Diagram在visio页面中绘制三角形。支持使用C#绘制三角形并保存为pdf、svg、html、image、xps等格式。
---
## **在 Visio 中绘制三角形**
Aspose.Diagram for .NET API 允许开发人员在页面中绘制三角形。下面的代码示例显示了如何在 Visio 绘图中绘制三角形。

```
{{< highlight "csharp" >}}
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
```

## **在 SVG 中绘制三角形**
Aspose.Diagram for .NET API allows developers to draw a triangle in the page and save as SVG format. The code example below shows how to draw a triangle in a Visio drawing and save as SVG format.

```
{{< highlight "csharp" >}}
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
```

## **在 PDF 中绘制三角形**
Aspose.Diagram for .NET API allows developers to draw a triangle in the page and save as PDF format. The code example below shows how to draw a triangle in a Visio drawing and save as PDF format.

```
{{< highlight "csharp" >}}
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
```

## **在 PNG 中绘制三角形**
Aspose.Diagram for .NET API allows developers to draw a triangle in the page and save as PNG format. The code example below shows how to draw a triangle in a Visio drawing and save as PNG format.

```
{{< highlight "csharp" >}}
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
```

## **在 HTML 中绘制三角形**
Aspose.Diagram for .NET API allows developers to draw a triangle in the page and save as HTML format. The code example below shows how to draw a triangle in a Visio drawing and save as HTML format.

```
{{< highlight "csharp" >}}
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
```
