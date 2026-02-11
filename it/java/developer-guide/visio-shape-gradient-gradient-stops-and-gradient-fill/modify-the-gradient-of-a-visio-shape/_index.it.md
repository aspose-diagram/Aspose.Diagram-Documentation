---
title: Modifica il gradiente di una forma Visio
type: docs
weight: 10
url: /it/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

Utilizzando Aspose.Diagram API, gli sviluppatori possono migliorare l'aspetto di una forma Visio modificando le proprietà del gradiente. Gli sviluppatori possono recuperare un riempimento sfumato per impostare la direzione, l'angolo, il colore e la posizione dell'interruzione del gradiente, ecc.

{{% /alert %}} 
## **Modificare l'esempio di programmazione del riempimento sfumato**
[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)offre la proprietà Fill che consente agli sviluppatori di recuperare un file[GradientFill](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)oggetto. La classe GradientFill contiene i dati del gradiente di una forma Visio. Gli sviluppatori possono impostare tutte le sue proprietà disponibili e recuperare un gradiente in base all'indice per impostare le proprietà di colore e posizione.

```
{{< highlight "java" >}}
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(ModifyShapeGradientFill.class) + "ShapeGradientFill\\";

// load a Visio drawing
Diagram diagram = new Diagram(dataDir + "ShapewithGradientFill.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// get the gradient fill properties
GradientFill gradientfill = shape.getFill().getGradientFill();
// get the gradient stops
GradientStopCollection stops = gradientfill.getGradientStops();
// get the gradient stop by index
GradientStop stop = stops.get(0);
// set gradient stop properties
stop.getColor().getUfe().setF("");
stop.getPosition().setValue(0.5);
gradientfill.getGradientDir().setValue(GradientFillDir.RECTANGLE_FROM_BOTTOM_RIGHT);
gradientfill.getGradientAngle().setValue(0.7853981633974501);
// save the Visio drawing
diagram.save(dataDir + "ShapewithGradientFill_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```
