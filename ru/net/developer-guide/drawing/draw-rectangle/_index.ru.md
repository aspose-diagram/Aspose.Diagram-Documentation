---
title: Нарисовать прямоугольник
type: docs
weight: 10
url: /ru/net/drawing/draw-rectangle
description: В этом разделе объясняется, как нарисовать прямоугольник на странице visio с помощью Aspose.Diagram. Поддержка использования C# для рисования прямоугольника и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
## **Нарисовать прямоугольник в Visio**
Aspose.Diagram for .NET API позволяет разработчикам рисовать прямоугольник на странице. В приведенном ниже примере кода показано, как нарисовать прямоугольник на чертеже Visio.


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


## **Нарисовать прямоугольник в SVG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать прямоугольник на странице и сохранять в формате SVG. В приведенном ниже примере кода показано, как нарисовать прямоугольник на чертеже Visio и сохранить его в формате SVG.


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


## **Нарисовать прямоугольник в PDF**
Aspose.Diagram for .NET API позволяет разработчикам рисовать прямоугольник на странице и сохранять в формате PDF. В приведенном ниже примере кода показано, как нарисовать прямоугольник на чертеже Visio и сохранить его в формате PDF.


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


## **Нарисовать прямоугольник в PNG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать прямоугольник на странице и сохранять в формате PNG. В приведенном ниже примере кода показано, как нарисовать прямоугольник на чертеже Visio и сохранить его в формате PNG.


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


## **Нарисовать прямоугольник в HTML**
Aspose.Diagram for .NET API позволяет разработчикам рисовать прямоугольник на странице и сохранять в формате HTML. В приведенном ниже примере кода показано, как нарисовать прямоугольник на чертеже Visio и сохранить его в формате HTML.


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

