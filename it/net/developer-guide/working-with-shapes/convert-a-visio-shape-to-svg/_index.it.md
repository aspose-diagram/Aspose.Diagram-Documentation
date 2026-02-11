---
title: Converti una forma Visio in Svg
type: docs
weight: 10
url: /it/net/convert-a-visio-shape-to-svg/
description: Questa sezione spiega come convertire una forma visio in svg con Aspose.Diagram.
---
## ** Converti una forma visio in svg**
 Il metodo ToSvg esposto da[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class può essere utilizzato per convertire in svg.

Il codice seguente mostra come:

1. Carica un campione diagram.
1. ottenere una pagina particolare.
1. ottenere una forma particolare.
1. convertire la forma in svg.
### **Forma in formato Svg**
Usa il seguente codice nella tua applicazione .net per convertire una forma visio in svg.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToSvg.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

SVGSaveOptions svgOptions = new SVGSaveOptions();
// Shape to Svg
shape.ToSvg("out.svg",svgOptions);

{{< /highlight >}}
```

