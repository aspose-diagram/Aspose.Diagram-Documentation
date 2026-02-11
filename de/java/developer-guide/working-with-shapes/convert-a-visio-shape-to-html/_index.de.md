---
title: Konvertieren Sie eine Visio-Form in HTML
type: docs
weight: 10
url: /de/java/convert-a-visio-shape-to-html/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram in HTML konvertieren.
---
## ** Konvertieren Sie eine visio-Form in HTML**
 Die ToHTML-Methode, die von der bereitgestellt wird[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) Klasse kann zum Konvertieren in HTML verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Form in html umwandeln.
### **Form zu HTML**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine visio-Form in HTML zu konvertieren.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToHtml.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to HTML
HTMLSaveOptions hs = new HTMLSaveOptions();
shape.toHTML("out.htm", hs);
{{< /highlight >}}



