---
title: Нарисуй алмаз
type: docs
weight: 30
url: /ru/net/drawing/draw-diamond
description: В этом разделе объясняется, как нарисовать ромб на странице visio с помощью Aspose.Diagram. Поддерживается использование C# для рисования ромба и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
## **Нарисуйте алмаз в Visio**
Aspose.Diagram for .NET API позволяет разработчикам рисовать ромб на странице. В приведенном ниже примере кода показано, как нарисовать ромб на рисунке Visio.


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


## **Нарисуйте алмаз в SVG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать ромб на странице и сохранять в формате SVG. В приведенном ниже примере кода показано, как нарисовать ромб на чертеже Visio и сохранить его в формате SVG.


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


## **Нарисуйте алмаз в PDF**
Aspose.Diagram for .NET API позволяет разработчикам рисовать ромб на странице и сохранять в формате PDF. В приведенном ниже примере кода показано, как нарисовать ромб на чертеже Visio и сохранить его в формате PDF.


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


## **Нарисуйте алмаз в PNG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать ромб на странице и сохранять в формате PNG. В приведенном ниже примере кода показано, как нарисовать ромб на чертеже Visio и сохранить его в формате PNG.


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


## **Нарисуйте алмаз в HTML**
Aspose.Diagram for .NET API позволяет разработчикам рисовать ромб на странице и сохранять в формате HTML. В приведенном ниже примере кода показано, как нарисовать ромб на чертеже Visio и сохранить его в формате HTML.


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

