---
title: Konvertieren Sie eine Visio-Form in ein SVG-Format
type: docs
weight: 10
url: /de/net/convert-a-visio-shape-to-svg/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram in SVG konvertieren.
---
## ** Konvertieren Sie eine visio-Form in SVG**
 Die ToSvg-Methode, die von der[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse kann zum Konvertieren in SVG verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Konvertieren Sie die Form in SVG.
### **Form zu Svg**
Verwenden Sie den folgenden Code in Ihrer .net-Anwendung, um eine visio-Form in SVG zu konvertieren.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}
```

