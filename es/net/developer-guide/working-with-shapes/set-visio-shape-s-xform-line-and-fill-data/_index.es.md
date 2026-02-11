---
title: Establecer Visio Forma XForm, Línea y Datos de relleno
type: docs
weight: 20
url: /es/net/set-visio-shape-s-xform-line-and-fill-data/
description: Esta sección explica cómo configurar el estilo de la forma, incluidos sus datos de línea y datos de relleno con Aspose.Diagram.
---
## **Configuración de datos de XForm**
 El elemento XForm es parte del esquema XML Microsoft Visio. XForm especifica la posición de una forma, por ejemplo, ancho, alto, rotación y si la forma ha sido volteada. los[Formulario X](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) propiedad expuesta por la[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, admite el objeto Aspose.Diagram.XForm. La propiedad XForm se puede usar para recuperar o actualizar los datos XForm de una forma. Los ejemplos de código de este artículo cambian los valores de XForm PinX (coordenada X) y PinY (coordenada Y) para mover las formas en la página.

El proceso para actualizar los datos de XForm es:

1. Cargue un diagram.# Encuentre una forma particular.# Actualice los datos XForm de la forma.
1. Guarda el diagram.
### **Ejemplo de programación**
El fragmento de código a continuación muestra cómo actualizar los datos XForm de una forma. El código busca un proceso de nombres de forma, con el ID de forma 1, y establece sus coordenadas X e Y en 5.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.XForm.PinX.Value = 5;
        shape.XForm.PinY.Value = 5;
    }
}
// Save diagram
diagram.Save(dataDir + "SetXFormdata_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Establecer Visio datos de línea de forma**
Las formas se pueden formatear de varias maneras. Este artículo muestra cómo especificar los atributos de una línea.

Microsoft Visio permite a los usuarios dar formato a las líneas de varias formas. Aspose.Diagram for .NET admite:

- Peso: el grosor de una línea.
- Color: establezca el color de línea de la forma.
- Transparencia de color de línea: establezca la transparencia de color de línea de la forma en porcentaje.
- Patrón: define si la línea es sólida, discontinua o tiene otro patrón.
- Redondeo: el radio de las esquinas.
- Flechas de inicio y fin: especifica si la línea tiene flechas.
- Tamaños de flecha inicial y final: establezca los tamaños de flecha.
- Cap: el redondeo de los extremos de la línea.
### **Cambie el color de línea, el grosor, el tipo de guión, la transparencia, el redondeo, el tipo de flecha y el tamaño de flecha del borde de una forma**
 los[Línea](http://www.aspose.com/api/net/diagram/aspose.diagram/line) propiedad expuesta por la[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)clase, admite el objeto Aspose.Diagram.Line. Esta propiedad se puede usar para recuperar o actualizar los datos de línea de una forma.
#### **Ejemplo de programación de datos de línea**
El siguiente fragmento de código actualiza los datos de línea de forma.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set line dash type by index
shape.Line.LinePattern.Value = 4;
// Set line weight, defualt in inch
shape.Line.LineWeight.Value = 2;
// Set color of the shape's line
shape.Line.LineColor.Ufe.F = "RGB(95,108,53)";
// Set line rounding, default in inch
shape.Line.Rounding.Value = 0.3125;
// Set line caps
shape.Line.LineCap.Value = BOOL.True;
// Set line color transparency in percent
shape.Line.LineColorTrans.Value = 50;

/* add arrows to the connector or curve shapes */
// Select arrow type by index
shape.Line.BeginArrow.Value = 4;
shape.Line.EndArrow.Value = 4;
// Set arrow size 
shape.Line.BeginArrowSize.Value = ArrowSizeValue.Large;
shape.Line.EndArrowSize.Value = ArrowSizeValue.Large;

// Save the Visio
diagram.Save(dataDir + "SetLineData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Establecer los datos de relleno de la forma Visio**
 Las formas se pueden formatear de varias maneras. Este tema describe cómo especificar el relleno de una forma. Microsoft Office Visio permite a los usuarios dar formato a los rellenos de varias formas. los[Llenar](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) La clase de Aspose.Diagram for .NET API admite la configuración:

- Colores de fondo y de primer plano.
- Transparencia.
- Patrones de relleno.
- Oscuridad.
### **Configuración de valores de relleno**
 La propiedad Relleno, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, apoya la[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) objeto. La propiedad Relleno se puede utilizar para recuperar o actualizar los datos de relleno de una forma.
#### **Ejemplo de programación de datos de relleno**
El siguiente fragmento de código actualiza los datos de relleno de una forma. El código busca una forma denominada rectángulo, con el Id. de forma 1, y establece los colores de fondo y de primer plano del relleno.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetFillData.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "rectangle" && shape.ID == 1)
    {
        shape.Fill.FillBkgnd.Value = diagram.Pages[1].Shapes[0].Fill.FillBkgnd.Value;
        shape.Fill.FillForegnd.Value = "#ebf8df";
    }
}
// Save diagram
diagram.Save(dataDir + "SetFillData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Recuperar datos de relleno heredados de una forma Visio**
 Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de relleno heredados de una forma Visio. La propiedad InheritFill, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, contiene los valores de formato de relleno para la forma heredada por el estilo principal y la forma maestra.
#### **Recuperar muestra de programación de datos de llenado heredados**
El siguiente fragmento de código recupera los datos de relleno heredados de la forma. Por favor revise este código de muestra:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwObliqueAngle.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetX.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetY.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwScaleFactor.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwType.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgnd.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwForegnd.Value);
Console.WriteLine(shape.InheritFill.ShdwForegndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwPattern.Value);

{{< /highlight >}}
```
