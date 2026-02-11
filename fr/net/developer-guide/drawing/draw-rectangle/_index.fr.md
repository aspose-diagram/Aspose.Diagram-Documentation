---
title: Dessiner un rectangle
type: docs
weight: 10
url: /fr/net/drawing/draw-rectangle
description: Cette section explique comment dessiner un rectangle dans une page visio avec Aspose.Diagram. Prise en charge de l'utilisation de C# pour dessiner un rectangle et l'enregistrer au format pdf, svg, html, image, xps et autres formats.
---
## **Dessiner un rectangle en Visio**
Aspose.Diagram for .NET API permet aux développeurs de dessiner une forme de rectangle dans une page. L'exemple de code ci-dessous montre comment dessiner un rectangle dans un dessin Visio.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner un rectangle en SVG**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as SVG format. The code example below shows how to draw a rectangle in a Visio drawing and save as SVG format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner un rectangle en PDF**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as PDF format. The code example below shows how to draw a rectangle in a Visio drawing and save as PDF format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner un rectangle en PNG**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as PNG format. The code example below shows how to draw a rectangle in a Visio drawing and save as PNG format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner un rectangle en HTML**
Aspose.Diagram for .NET API allows developers to draw a rectangle in the page and save as HTML format. The code example below shows how to draw a rectangle in a Visio drawing and save as HTML format.

```
{{< highlight "csharp" >}}
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
```
