---
title: Rita rektangel
type: docs
weight: 10
url: /sv/net/drawing/draw-rectangle
description: Det här avsnittet förklarar hur man ritar rektangel på en visio-sida med Aspose.Diagram. Stöd att använda C# för att rita rektangel och spara som pdf, svg, html, bild, xps och andra format.
---
## **Rita rektangel i Visio**
Aspose.Diagram for .NET API tillåter utvecklare att rita en rektangelform på en sida. Kodexemplet nedan visar hur man ritar en rektangel i en Visio-ritning.

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

## **Rita rektangel i SVG**
Aspose.Diagram for .NET API låter utvecklare rita en rektangel på sidan och spara som SVG-format. Kodexemplet nedan visar hur man ritar en rektangel i en Visio-ritning och sparar som SVG-format.

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

## **Rita rektangel i PDF**
Aspose.Diagram for .NET API låter utvecklare rita en rektangel på sidan och spara som PDF-format. Kodexemplet nedan visar hur man ritar en rektangel i en Visio-ritning och sparar som PDF-format.

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

## **Rita rektangel i PNG**
Aspose.Diagram for .NET API låter utvecklare rita en rektangel på sidan och spara som PNG-format. Kodexemplet nedan visar hur man ritar en rektangel i en Visio-ritning och sparar som PNG-format.

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

## **Rita rektangel i HTML**
Aspose.Diagram for .NET API låter utvecklare rita en rektangel på sidan och spara som HTML-format. Kodexemplet nedan visar hur man ritar en rektangel i en Visio-ritning och sparar som HTML-format.

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
