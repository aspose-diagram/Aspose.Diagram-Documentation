---
title: Converti una forma Visio in PDF
type: docs
weight: 10
url: /it/java/convert-a-visio-shape-to-pdf/
description: Questa sezione spiega come convertire una forma visio in pdf con Aspose.Diagram.
---
## ** Converti una forma visio in pdf**
 Il metodo ToPdf esposto da[Forma](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) class può essere utilizzato per convertire in pdf.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in pdf.
### **Forma in Pdf**
Usa il seguente codice nella tua applicazione java per convertire una forma visio in pdf.


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



