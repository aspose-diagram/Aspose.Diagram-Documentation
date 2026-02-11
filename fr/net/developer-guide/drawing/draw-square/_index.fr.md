---
title: Dessiner un carré
type: docs
weight: 50
url: /fr/net/drawing/draw-square
description: Cette section explique comment dessiner un carré dans une page visio avec Aspose.Diagram. Prise en charge de l'utilisation de C# pour dessiner un carré et l'enregistrer au format pdf, svg, html, image, xps et autres formats.
---
## **Dessiner carré en Visio**
Aspose.Diagram for .NET API permet aux développeurs de dessiner une forme carrée dans une page. L'exemple de code ci-dessous montre comment dessiner un carré dans un dessin Visio.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner carré en SVG**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as SVG format. The code example below shows how to draw a square in a Visio drawing and save as SVG format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner carré en PDF**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as PDF format. The code example below shows how to draw a square in a Visio drawing and save as PDF format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner carré en PNG**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as PNG format. The code example below shows how to draw a square in a Visio drawing and save as PNG format.

```
{{< highlight "csharp" >}}
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
```

## **Dessiner carré en HTML**
Aspose.Diagram for .NET API allows developers to draw a square in the page and save as HTML format. The code example below shows how to draw a square in a Visio drawing and save as HTML format.

```
{{< highlight "csharp" >}}
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
```
