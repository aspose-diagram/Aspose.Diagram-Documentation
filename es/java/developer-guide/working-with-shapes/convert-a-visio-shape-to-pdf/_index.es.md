---
title: Convertir una forma Visio a PDF
type: docs
weight: 10
url: /es/java/convert-a-visio-shape-to-pdf/
description: Esta sección explica cómo convertir una forma visio a pdf con Aspose.Diagram.
---
## ** Convertir una forma visio a pdf**
 El método ToPdf expuesto por el[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) La clase se puede utilizar para convertir a pdf.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma a pdf.
### **Forma a PDF**
Use el siguiente código en su aplicación java para convertir una forma visio a pdf.

```
{{< highlight "java" >}}
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
```


