---
title: Нарисовать квадрат
type: docs
weight: 50
url: /ru/net/drawing/draw-square
description: В этом разделе объясняется, как нарисовать квадрат на странице visio с помощью Aspose.Diagram. Поддержка использования C# для рисования квадрата и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
## **Нарисуйте квадрат в Visio**
Aspose.Diagram for .NET API позволяет разработчикам рисовать квадрат на странице. В приведенном ниже примере кода показано, как нарисовать квадрат на чертеже Visio.


{{< highlight csharp >}}
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


## **Нарисуйте квадрат в SVG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать квадрат на странице и сохранять в формате SVG. В приведенном ниже примере кода показано, как нарисовать квадрат на чертеже Visio и сохранить его в формате SVG.


{{< highlight csharp >}}
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


## **Нарисуйте квадрат в PDF**
Aspose.Diagram for .NET API позволяет разработчикам рисовать квадрат на странице и сохранять в формате PDF. В приведенном ниже примере кода показано, как нарисовать квадрат на чертеже Visio и сохранить его в формате PDF.


{{< highlight csharp >}}
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


## **Нарисуйте квадрат в PNG**
Aspose.Diagram for .NET API позволяет разработчикам рисовать квадрат на странице и сохранять в формате PNG. В приведенном ниже примере кода показано, как нарисовать квадрат на чертеже Visio и сохранить его в формате PNG.


{{< highlight csharp >}}
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


## **Нарисуйте квадрат в HTML**
Aspose.Diagram for .NET API позволяет разработчикам рисовать квадрат на странице и сохранять в формате HTML. В приведенном ниже примере кода показано, как нарисовать квадрат на чертеже Visio и сохранить его в формате HTML.


{{< highlight csharp >}}
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

