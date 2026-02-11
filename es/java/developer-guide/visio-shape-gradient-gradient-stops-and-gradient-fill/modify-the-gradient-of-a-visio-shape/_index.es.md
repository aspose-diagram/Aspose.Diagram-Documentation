---
title: Modificar el degradado de una forma Visio
type: docs
weight: 10
url: /es/java/modify-the-gradient-of-a-visio-shape/
---
{{% alert color="primary" %}} 

Con Aspose.Diagram API, los desarrolladores pueden mejorar la apariencia de una forma Visio modificando las propiedades del degradado. Los desarrolladores pueden recuperar un relleno degradado para establecer la dirección, el ángulo, el color y la posición de parada del degradado, etc.

{{% /alert %}} 
## **Modificar el ejemplo de programación de relleno de degradado**
[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)class ofrece la propiedad Fill que permite a los desarrolladores recuperar un[Relleno degradado](https://reference.aspose.com/diagram/java/com.aspose.diagram/gradientfill)objeto. La clase GradientFill contiene los datos de degradado de una forma Visio. Los desarrolladores pueden establecer todas sus propiedades disponibles, así como recuperar un degradado por índice para establecer las propiedades de color y posición.


{{< highlight java >}}
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

