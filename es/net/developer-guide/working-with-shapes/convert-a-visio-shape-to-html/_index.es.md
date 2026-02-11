---
title: Convertir una forma Visio a Html
type: docs
weight: 10
url: /es/net/convert-a-visio-shape-to-html/
description: Esta sección explica cómo convertir una forma visio a html con Aspose.Diagram.
---
## ** Convierte una forma visio a html**
 El método ToHTML expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede usar para convertir a html.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. convertir forma a html.
### **Forma a Html**
Use el siguiente código en su aplicación .net para convertir una forma visio a html.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}


