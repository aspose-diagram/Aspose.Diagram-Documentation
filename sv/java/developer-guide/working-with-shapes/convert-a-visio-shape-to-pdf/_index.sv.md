---
title: Konvertera en Visio form till pdf
type: docs
weight: 10
url: /sv/java/convert-a-visio-shape-to-pdf/
description: Det här avsnittet förklarar hur man konverterar en visio-form till pdf med Aspose.Diagram.
---
## ** Konvertera en visio-form till pdf**
 ToPdf-metoden exponerad av[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) klass kan användas för att konvertera till pdf.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell form.
1. konvertera form till pdf.
### **Form till pdf**
Använd följande kod i din java-applikation för att konvertera en visio-form till pdf.

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


