---
title: Konvertieren Sie eine Visio-Form in ein Bild
type: docs
weight: 10
url: /de/net/convert-a-visio-shape-to-image/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form in ein Bild mit Aspose.Diagram konvertieren.
---
## **Konvertieren Sie eine visio-Form in ein Bild**
In diesem Thema wird erläutert, wie Entwickler eine visio-Form mithilfe von Aspose.Diagram in ein Bild konvertieren können.
 Die ToImage-Methode, die von der[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse kann zum Konvertieren in ein Bild verwendet werden.


Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Form in Bild umwandeln.
#### **Shape to image Programmierbeispiel**
Verwenden Sie den folgenden Code in Ihrer .net-Anwendung, um eine visio-Form in ein Bild zu konvertieren.


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

