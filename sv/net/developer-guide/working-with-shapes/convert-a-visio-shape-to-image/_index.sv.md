---
title: Konvertera en Visio form till bild
type: docs
weight: 10
url: /sv/net/convert-a-visio-shape-to-image/
description: Det här avsnittet förklarar hur du konverterar en visio-form till en bild med Aspose.Diagram.
---
## **Konvertera en visio-form till bild**
Det här ämnet utvecklar hur utvecklare kan konvertera en visio-form till bild med Aspose.Diagram.
 ToImage-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass kan användas för att konvertera till bild.


Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. konvertera form till bild.
#### **Form till bild Programmeringsexempel**
Använd följande kod i din .net-applikation för att konvertera en visio-form till en bild.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}

