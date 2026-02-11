---
title: Converti una forma Visio in Svg
type: docs
weight: 10
url: /it/java/convert-a-visio-shape-to-svg/
description: Questa sezione spiega come convertire una forma visio in svg con Aspose.Diagram.
---
## ** Converti una forma visio in svg**
 Il metodo ToSvg esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class può essere utilizzato per convertire in svg.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in svg.
### **Forma in formato Svg**
Utilizzare il codice seguente nell'applicazione Java per convertire una forma visio in svg.

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


