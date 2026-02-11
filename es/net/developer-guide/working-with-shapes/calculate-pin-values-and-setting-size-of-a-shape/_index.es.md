---
title: Calcule los valores de los pines y establezca el tamaño de una forma
type: docs
weight: 60
url: /es/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Esta sección explica cómo calcular los valores PinX y PinY de la forma secundaria con Aspose.Diagram.
---
## **Calcule los valores PinX y PinY de la forma secundaria**
 Si la forma es un nodo secundario de la forma del grupo, su forma x es una coordenada relativa de su forma principal, pero no una coordenada absoluta en el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Si el usuario necesita obtener la coordenada absoluta, entonces este código de muestra ayuda.

Un punto especificado en coordenadas locales se puede convertir en coordenadas principales aplicando las siguientes transformaciones en el siguiente orden:

1. Reste el valor de la propiedad LocPinX del elemento Cell_Type de la coordenada x.
1. Reste el valor de la propiedad LocPinY de Cell_Type de la coordenada y.
1. Refleje el punto sobre el eje y si el valor de la propiedad FlipX de Cell_Type es igual a uno.
1. Refleje el punto sobre el eje x si el valor de la propiedad FlipY de Cell_Type es igual a uno.
1. Gire el punto en sentido contrario a las agujas del reloj alrededor del origen según el valor de la propiedad Angle de Cell_Type.
1. Agregue el valor de PinX Cell_Type a la coordenada x.
1. Agregue el valor de PinY Cell_Type a la coordenada y.
### **Ejemplo de programación Calcular PinX y PinY**
Use el siguiente código en su aplicación .NET para calcular los valores PinX y PinY de una subforma usando Aspose.Diagram for .NET API.








{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get a group shape by ID and page index is 0
Shape shape = diagram.Pages[0].Shapes.GetShape(795);
// Get a sub-shape of the group shape by id
Shape subShape = shape.Shapes.GetShape(794);

Matrix m = new Matrix();
// Apply the translation vector
m.Translate(-(float)subShape.XForm.LocPinX.Value, -(float)subShape.XForm.LocPinY.Value);
// Set the elements of that matrix to a rotation
m.Rotate((float)subShape.XForm.Angle.Value);
// Apply the translation vector
m.Translate((float)subShape.XForm.PinX.Value, (float)subShape.XForm.PinY.Value);

// Get pinx and piny
double pinx = m.OffsetX;
double piny = m.OffsetY;
// Calculate the sub-shape pinx and piny
double resultx = shape.XForm.PinX.Value - shape.XForm.LocPinX.Value - pinx;
double resulty = shape.XForm.PinY.Value - shape.XForm.LocPinY.Value - piny;

{{< /highlight >}}

## **Establecer la altura y el ancho de una forma**
 los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Class le permite controlar el tamaño de la forma especificando la altura y el ancho de la forma mediante los métodos SetHeight y SetWidth.

 Los métodos SetHeight y SetWidth, expuestos por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)clase, admite cambiar el tamaño de una forma con el maestro, sin el maestro o en forma de forma de grupo. Los ejemplos de código de este artículo establecen el alto y el ancho para cambiar el tamaño de la forma en la página.

El proceso para configurar Alto y Ancho es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Establecer la altura de una forma.
1. Establezca el Ancho de una forma.
1. Guarda el diagram.
### **Ejemplo de programación de ajuste de altura y anchura**
El fragmento de código a continuación muestra cómo establecer la altura y el ancho de la forma. El código busca un rectángulo de nombre de forma, con el ID de forma 1, y establece su Alto y Ancho como doble.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by id
Shape shape = page.Shapes.GetShape(796);
// Alter the size of Shape
shape.SetWidth(2 * shape.XForm.Width.Value);
shape.SetHeight(2 * shape.XForm.Height.Value);
// Save diagram
diagram.Save(dataDir + "ChangeShapeSize_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

