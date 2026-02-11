---
title: Нарисовать треугольник
type: docs
weight: 60
url: /ru/net/drawing/draw-triangle
description: В этом разделе объясняется, как нарисовать треугольник на странице visio с помощью Aspose.Diagram. Поддержка использования C# для рисования треугольника и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
## **Нарисуйте треугольник в Visio**
Aspose.Diagram for .NET API позволяет разработчикам рисовать треугольник на странице. В приведенном ниже примере кода показано, как нарисовать треугольник на чертеже Visio.


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


## **Нарисуйте треугольник в SVG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать треугольник на странице и сохранять в формате SVG. В приведенном ниже примере кода показано, как нарисовать треугольник на чертеже Visio и сохранить его в формате SVG.


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


## **Нарисуйте треугольник в PDF**
Aspose.Diagram for .NET API позволяет разработчикам рисовать треугольник на странице и сохранять в формате PDF. В приведенном ниже примере кода показано, как нарисовать треугольник на чертеже Visio и сохранить его в формате PDF.


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


## **Нарисуйте треугольник в PNG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать треугольник на странице и сохранять в формате PNG. В приведенном ниже примере кода показано, как нарисовать треугольник на чертеже Visio и сохранить его в формате PNG.


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


## **Нарисуйте треугольник в HTML**
Aspose.Diagram for .NET API позволяет разработчикам рисовать треугольник на странице и сохранять в формате HTML. В приведенном ниже примере кода показано, как нарисовать треугольник на чертеже Visio и сохранить его в формате HTML.


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

