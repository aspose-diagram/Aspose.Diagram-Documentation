---
title: Konvertieren Sie eine Visio-Form in ein SVG-Format
type: docs
weight: 10
url: /de/java/convert-a-visio-shape-to-svg/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram in SVG konvertieren.
---
## ** Konvertieren Sie eine visio-Form in SVG**
 Die ToSvg-Methode, die von der[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Klasse kann zum Konvertieren in SVG verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Konvertieren Sie die Form in SVG.
### **Form zu Svg**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine visio-Form in SVG zu konvertieren.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToSvg.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Svg
SVGSaveOptions option = new SVGSaveOptions();
shape.toSvg("out.svg",option);
{{< /highlight >}}



