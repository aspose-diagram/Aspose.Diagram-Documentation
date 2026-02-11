---
title: Dessiner le Pentagone
type: docs
weight: 40
url: /fr/net/drawing/draw-pentagon
description: Cette section explique comment dessiner le pentagone dans une page visio avec Aspose.Diagram. Prise en charge de l'utilisation de C# pour dessiner le pentagone et l'enregistrer au format pdf, svg, html, image, xps et autres formats.
---
## **Dessiner le Pentagone en Visio**
Aspose.Diagram for .NET API permet aux développeurs de dessiner une forme de pentagone dans une page. L'exemple de code ci-dessous montre comment dessiner un pentagone dans un dessin Visio.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **Dessiner le Pentagone en SVG**
Aspose.Diagram for .NET API allows developers to draw a pentagon in the page and save as SVG format. The code example below shows how to draw a pentagon in a Visio drawing and save as SVG format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as SVG images
SVGSaveOptions imageSaveOptions = new SVGSaveOptions();
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.svg", imageSaveOptions);

{{< /highlight >}}
```

## **Dessiner le Pentagone en PDF**
Aspose.Diagram for .NET API allows developers to draw a pentagon in the page and save as PDF format. The code example below shows how to draw a pentagon in a Visio drawing and save as PDF format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.pdf", new PdfSaveOptions());

{{< /highlight >}}
```

## **Dessiner le Pentagone en PNG**
Aspose.Diagram for .NET API allows developers to draw a pentagon in the page and save as PNG format. The code example below shows how to draw a pentagon in a Visio drawing and save as PNG format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram as PNG image
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFileFormat.PNG);
imageSaveOptions.PageIndex = 0;
diagram.Save(dataDir + "DrawPentagonInPage_out.png", imageSaveOptions);

{{< /highlight >}}
```

## **Dessiner le Pentagone en HTML**
Aspose.Diagram for .NET API allows developers to draw a pentagon in the page and save as HTML format. The code example below shows how to draw a pentagon in a Visio drawing and save as HTML format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
//Initiazlie a new PointF[]
PointF[] ps = new PointF[] { new PointF(1, 1), new PointF(2, 1), new PointF(2.309f, 1.951f), new PointF(1.5f, 2.54f), new PointF(0.691f, 1.951f), new PointF(1, 1) };
//Draw Pentagon in page
diagram.Pages[0].DrawPolyline(1, 1, 2, 2, ps);

// Save diagram
diagram.Save(dataDir + "DrawPentagonInPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```
