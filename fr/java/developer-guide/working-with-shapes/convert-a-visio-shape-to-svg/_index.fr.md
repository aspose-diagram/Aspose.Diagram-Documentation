---
title: Convertir une forme Visio en Svg
type: docs
weight: 10
url: /fr/java/convert-a-visio-shape-to-svg/
description: Cette section explique comment convertir une forme visio en svg avec Aspose.Diagram.
---
## ** Convertir une forme visio en svg**
 La méthode ToSvg exposée par le[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) la classe peut être utilisée pour convertir en svg.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. convertir la forme en svg.
### **Forme en Svg**
Utilisez le code suivant dans votre application Java pour convertir une forme visio en svg.

```
{{< highlight "java" >}}
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
```


