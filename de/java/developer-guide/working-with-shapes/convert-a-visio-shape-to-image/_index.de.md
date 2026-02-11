---
title: Konvertieren Sie eine Visio-Form in ein Bild
type: docs
weight: 10
url: /de/java/convert-a-visio-shape-to-image/
description: In diesem Abschnitt wird erläutert, wie Sie eine visio-Form in ein Bild mit Aspose.Diagram konvertieren.
---
## **Konvertieren Sie eine visio-Form in ein Bild**
 Die ToImage-Methode, die von der[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) Klasse kann zum Konvertieren in ein Bild verwendet werden.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. eine bestimmte Form bekommen.
1. Form in Bild umwandeln.
### **Zum Bild formen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um eine visio-Form in ein Bild zu konvertieren.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}
```


