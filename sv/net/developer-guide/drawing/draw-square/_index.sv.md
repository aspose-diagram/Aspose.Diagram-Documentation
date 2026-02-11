---
title: Rita fyrkant
type: docs
weight: 50
url: /sv/net/drawing/draw-square
description: Det här avsnittet förklarar hur man ritar kvadrat på en visio-sida med Aspose.Diagram. Stöd att använda C# för att rita kvadrat och spara som pdf, svg, html, bild, xps och andra format.
---
## **Rita Square på Visio**
Aspose.Diagram for .NET API tillåter utvecklare att rita en kvadratisk form på en sida. Kodexemplet nedan visar hur man ritar en kvadrat i en Visio-ritning.

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

## **Rita Square på SVG**
Aspose.Diagram for .NET API låter utvecklare rita en kvadrat på sidan och spara som SVG-format. Kodexemplet nedan visar hur man ritar en kvadrat i en Visio-ritning och sparar som SVG-format.

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

## **Rita Square på PDF**
Aspose.Diagram for .NET API låter utvecklare rita en kvadrat på sidan och spara som PDF-format. Kodexemplet nedan visar hur man ritar en kvadrat i en Visio-ritning och sparar som PDF-format.

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

## **Rita Square på PNG**
Aspose.Diagram for .NET API låter utvecklare rita en kvadrat på sidan och spara som PNG-format. Kodexemplet nedan visar hur man ritar en kvadrat i en Visio-ritning och sparar som PNG-format.

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

## **Rita Square på HTML**
Aspose.Diagram for .NET API låter utvecklare rita en kvadrat på sidan och spara som HTML-format. Kodexemplet nedan visar hur man ritar en kvadrat i en Visio-ritning och sparar som HTML-format.

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
