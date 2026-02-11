---
title: Infoga bild
type: docs
weight: 70
url: /sv/net/drawing/insert-image
description: Det här avsnittet förklarar hur man infogar en bild på en visio-sida med Aspose.Diagram. Stöd att använda C# för att infoga bild och spara som pdf, svg, html, bild, xps och andra format.
---
 De[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt.

## **Infoga bild i Visio**
Aspose.Diagram for .NET API tillåter utvecklare att infoga en bildform på en sida. Kodexemplet nedan visar hur man infogar en bild i en Visio-ritning.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

## **Infoga bild i SVG**
Aspose.Diagram for .NET API tillåter utvecklare att infoga en bildform på en sida. Kodexemplet nedan visar hur man infogar en bild i en Visio-ritning och sparar som SVG-format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```

## **Infoga bild i PNG**
Aspose.Diagram for .NET API tillåter utvecklare att infoga en bildform på en sida. Kodexemplet nedan visar hur man infogar en bild i en Visio-ritning och sparar som PNG-format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}
```

## **Infoga bild i PDF**
Aspose.Diagram for .NET API tillåter utvecklare att infoga en bildform på en sida. Kodexemplet nedan visar hur man infogar en bild i en Visio-ritning och sparar som PDF-format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```

## **Infoga bild i HTML**
Aspose.Diagram for .NET API tillåter utvecklare att infoga en bildform på en sida. Kodexemplet nedan visar hur man infogar en bild i en Visio-ritning och sparar som HTML-format.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}
```
