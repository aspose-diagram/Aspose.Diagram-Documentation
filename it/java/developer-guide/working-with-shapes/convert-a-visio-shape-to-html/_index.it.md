---
title: Converti una forma Visio in HTML
type: docs
weight: 10
url: /it/java/convert-a-visio-shape-to-html/
description: Questa sezione spiega come convertire una forma visio in html con Aspose.Diagram.
---
## ** Converti una forma visio in html**
 Il metodo ToHTML esposto da[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class può essere utilizzato per convertire in html.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in html.
### **Forma in Html**
Usa il seguente codice nella tua applicazione java per convertire una forma visio in html.

```
{{< highlight "java" >}}
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
```


