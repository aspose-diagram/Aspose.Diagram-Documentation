---
title: Konvertieren Sie eine Visio-Form in HTML
type: docs
weight: 10
url: /de/net/convert-a-visio-shape-to-html/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram in HTML konvertieren.
---
## ** Konvertieren Sie eine visio-Form in HTML**
 Die ToHTML-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klasse kann zum Konvertieren in HTML verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Form in html umwandeln.
### **Form zu HTML**
Verwenden Sie den folgenden Code in Ihrer .net-Anwendung, um eine visio-Form in HTML zu konvertieren.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}
```

