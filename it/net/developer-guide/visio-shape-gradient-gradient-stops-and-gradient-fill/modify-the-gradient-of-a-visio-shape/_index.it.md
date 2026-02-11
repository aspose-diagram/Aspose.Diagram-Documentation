---
title: Modifica il gradiente di una forma Visio
type: docs
weight: 10
url: /it/net/modify-the-gradient-of-a-visio-shape/
description: Questa pagina descrive come modificare il colore sfumato di una forma visio con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono migliorare l'aspetto di una forma Visio modificando le proprietà del gradiente. Gli sviluppatori possono recuperare un riempimento sfumato per impostare la direzione, l'angolo, il colore e la posizione dell'interruzione del gradiente, ecc.

{{% /alert %}} 
## **Modificare l'esempio di programmazione del riempimento sfumato**
[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)offre la proprietà Fill che consente agli sviluppatori di recuperare un file[GradientFill](http://www.aspose.com/api/net/diagram/aspose.diagram/gradientfill)oggetto. La classe GradientFill contiene i dati del gradiente di una forma Visio. Gli sviluppatori possono impostare tutte le sue proprietà disponibili e recuperare un gradiente in base all'indice per impostare le proprietà di colore e posizione.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeGradientFillData();
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape by ID
Aspose.Diagram.Shape shape = page.Shapes.GetShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.Fill.GradientFill;
// get the gradient stops
GradientStopCollection stops = gradientfill.GradientStops;
// get the gradient stop by index
GradientStop stop = stops[0];
// set gradient stop properties
stop.Color.Ufe.F = "";
stop.Position.Value = 0.5;
gradientfill.GradientDir.Value = (int)GradientFillDir.RectangleFromBottomRight;
gradientfill.GradientAngle.Value = 0.7853981633974501;
// save the Visio drawing
diagram.Save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
