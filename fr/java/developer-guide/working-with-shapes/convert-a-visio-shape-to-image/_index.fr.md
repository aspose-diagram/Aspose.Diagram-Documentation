---
title: Convertir une forme Visio en image
type: docs
weight: 10
url: /fr/java/convert-a-visio-shape-to-image/
description: Cette section explique comment convertir une forme visio en image avec Aspose.Diagram.
---
## **Convertir une forme visio en image**
 La méthode ToImage exposée par le[Forme](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class peut être utilisé pour convertir en image.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. convertir la forme en image.
### **Forme à l'image**
Utilisez le code suivant dans votre application Java pour convertir une forme visio en image.

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


