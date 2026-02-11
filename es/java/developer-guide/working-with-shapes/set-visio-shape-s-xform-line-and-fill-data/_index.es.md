---
title: Establecer Visio Forma XForm, Línea y Datos de relleno
type: docs
weight: 70
url: /es/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Configuración de datos de XForm**
 El elemento XForm es parte del esquema XML Microsoft Visio. XForm especifica la posición de una forma, por ejemplo, ancho, alto, rotación y si la forma ha sido volteada. los[Formulario X](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) propiedad expuesta por la[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) clase, admite el objeto Aspose.Diagram.XForm. La propiedad XForm se puede usar para recuperar o actualizar los datos XForm de una forma. Los ejemplos de código de este artículo cambian los valores de XForm PinX (coordenada X) y PinY (coordenada Y) para mover las formas en la página.

**Entrada diagram** 

![todo:imagen_alternativa_texto](set-visio-shape-s-xform-line-and-fill-data_1.png)

**El diagram después del** **PinX** **y** **PINY** **los valores han sido cambiados** 

![todo:imagen_alternativa_texto](set-visio-shape-s-xform-line-and-fill-data_2.png)

El proceso para actualizar los datos de XForm es:

1. Cargue un diagram.# Encuentre una forma particular.# Actualice los datos XForm de la forma.
1. Guarda el diagram.
### **Ejemplo de programación**
El fragmento de código a continuación muestra cómo actualizar los datos XForm de una forma. El código busca un proceso de nombres de forma, con el ID de forma 1, y establece sus coordenadas X e Y en 5.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Establecer Visio datos de línea de forma**
Las formas se pueden formatear de varias maneras. Este artículo muestra cómo especificar los atributos de una línea.

Microsoft Visio permite a los usuarios dar formato a las líneas de varias formas. Aspose.Diagram for Java admite:

- Peso: el grosor de una línea.
- Color: establezca el color de línea de la forma.
- Transparencia de color de línea: establezca la transparencia de color de línea de la forma en porcentaje.
- Patrón: define si la línea es sólida, discontinua o tiene otro patrón.
- Redondeo: el radio de las esquinas.
- Flechas de inicio y fin: especifica si la línea tiene flechas.
- Tamaños de flecha inicial y final: establezca los tamaños de flecha.
- Cap: el redondeo de los extremos de la línea.
### **Cambie el color de línea, el grosor, el tipo de guión, la transparencia, el redondeo, el tipo de flecha y el tamaño de flecha del borde de una forma**
 los[Línea](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) propiedad expuesta por la[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)clase, admite el objeto Aspose.Diagram.Line. Esta propiedad se puede usar para recuperar o actualizar los datos de línea de una forma.
#### **Ejemplo de programación de datos de línea**
El siguiente fragmento de código actualiza los datos de línea de forma.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Establecer los datos de relleno de la forma Visio**
Las formas se pueden formatear de varias maneras. Este tema describe cómo especificar el relleno de una forma.

 Microsoft Office Visio permite a los usuarios dar formato a los rellenos de varias formas. los[Llenar](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) La clase de Aspose.Diagram for Java API admite la configuración:

- Colores de fondo y de primer plano.
- Transparencia.
- Patrones de relleno.
- Oscuridad.
### **Configuración de valores de relleno**
La propiedad Fill, expuesta por la clase Shape, admite el objeto Aspose.Diagram.Fill. La propiedad Relleno se puede utilizar para recuperar o actualizar los datos de relleno de una forma.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/OrhEecb.png)</p>|<p>**El diagram después de cambiar el color de relleno** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Ejemplo de programación de datos de relleno**
El siguiente fragmento de código actualiza los datos de relleno de una forma. El código busca una forma denominada rectángulo, con el Id. de forma 1, y establece los colores de fondo y de primer plano del relleno.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **Recuperar datos de relleno heredados de una forma Visio**
Las formas Visio pueden heredar el estilo principal y la forma maestra. Los desarrolladores pueden obtener o configurar los datos de relleno heredados de una forma Visio. La propiedad InheritFill, expuesta por la clase Shape, contiene los valores de formato de relleno para la forma heredada por el estilo principal y la forma maestra.
#### **Recuperar muestra de programación de datos de llenado heredados**
El siguiente fragmento de código recupera los datos de relleno heredados de la forma. Por favor revise este código de muestra:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}

