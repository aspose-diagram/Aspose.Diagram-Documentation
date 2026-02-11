---
title: Converti una forma Visio in immagine
type: docs
weight: 10
url: /it/java/convert-a-visio-shape-to-image/
description: Questa sezione spiega come convertire una forma visio in un'immagine con Aspose.Diagram.
---
## **Converti una forma visio in immagine**
 Il metodo ToImage esposto da[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class può essere utilizzato per convertire in immagine.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in immagine.
### **Da forma a immagine**
Utilizzare il codice seguente nell'applicazione Java per convertire una forma visio in un'immagine.

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


