---
title: Convertir una forma Visio a Html
type: docs
weight: 10
url: /es/java/convert-a-visio-shape-to-html/
description: Esta sección explica cómo convertir una forma visio a html con Aspose.Diagram.
---
## ** Convierte una forma visio a html**
 El método ToHTML expuesto por el[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) La clase se puede usar para convertir a html.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma a html.
### **Forma a Html**
Use el siguiente código en su aplicación Java para convertir una forma visio a html.

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


