---
title: Konvertieren Sie eine Visio-Form in eine PDF-Datei
type: docs
weight: 10
url: /de/java/convert-a-visio-shape-to-pdf/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form mit Aspose.Diagram in eine PDF-Datei konvertieren.
---
## ** Konvertieren Sie eine visio-Form in eine PDF-Datei**
 Die ToPdf-Methode, die von der[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) Klasse kann zum Konvertieren in PDF verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Form in pdf umwandeln.
### **Form zu Pdf**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine visio-Form in eine PDF-Datei zu konvertieren.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToPdf.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Pdf
shape.toPdf("out.pdf");
{{< /highlight >}}



