---
title: Agregar, recuperar, copiar y leer datos de forma Visio
type: docs
weight: 10
url: /es/net/add-retrieve-copy-and-read-visio-shape-data/
description: Esta sección explica cómo agregar una forma, establecer la propiedad de la forma o copiar una forma con Aspose.Diagram.
---
## **Agregar una nueva forma en Visio**
Aspose.Diagram for .NET le permite manipular Microsoft Visio diagramas de diferentes maneras. Una de las cosas que puede hacer es agregar nuevas formas a los diagramas. Aspose.Diagram for .NET le permite agregar una nueva forma a un diagram. La forma agregada también se puede personalizar usando Aspose.Diagram for .NET.

Este tema describe cómo agregar una nueva forma de rectángulo a un diagram.

Use Aspose.Diagram for .NET API para crear nuevas formas y luego agregue estas formas a la colección de formas de diagram.

Para agregar una nueva forma:

1. **Encuentra la página** - Cada Visio diagram contiene una colección de páginas. Los desarrolladores pueden recuperar la página por ID o nombre de página y almacenar la página requerida en el[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objeto de clase.
1. **Agregue el maestro requerido de una forma** - Cada Visio diagram contiene una colección de maestros. Los desarrolladores pueden agregar un maestro (por ID o nombre) del archivo de plantilla existente (por ruta directa o flujo de archivo).
1. **Añadir forma en el Visio diagram** - Los desarrolladores pueden colocar una nueva forma en el Visio diagram por índice de página (a partir de 0), nombre maestro, PinX, PinY, alto (opcional) y ancho (opcional).
1. **Establecer propiedades de forma** - El método AddShape de la clase Diagram devuelve el ID de la forma. Los desarrolladores pueden recuperar la forma de un Visio diagram usando este ID y luego establecer sus propiedades, por ejemplo, color, posición, alineación y texto.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**El diagram con una forma añadida** </p><p>![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Agregar muestra de programación**
El fragmento de código a continuación muestra cómo hacer cada paso.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);
            
// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);
            
// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);
rectangle.XForm.PinX.Value = 5;
rectangle.XForm.PinY.Value = 5;
rectangle.Type = TypeValue.Shape;
rectangle.Text.Value.Add(new Txt("Aspose Diagram"));
rectangle.TextStyle = diagram.StyleSheets[3];
rectangle.Line.LineColor.Value = "#ff0000";
rectangle.Line.LineWeight.Value = 0.03;
rectangle.Line.Rounding.Value = 0.1;
rectangle.Fill.FillBkgnd.Value = "#ff00ff";
rectangle.Fill.FillForegnd.Value = "#ebf8df";

diagram.Save(dataDir + "AddShape_out.vsdx", SaveFileFormat.VSDX);
Console.WriteLine("Shape has been added.");

{{< /highlight >}}


{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Recuperación de información de forma**
[Trabajar con diagramas](/diagram/es/net/working-with-diagrams/)explica cómo crear diagramas, agregar formas y conectores, y luego cómo recuperar información sobre diagram elementos como[paginas](/diagram/es/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [maestros](https://docs.aspose.com/diagram/net/working-with-masters/), [conectores](/diagram/es/net/retrieving-connector-information/) y[fuentes](/diagram/es/net/retrieving-font-information/). Este artículo analiza cómo recuperar información sobre formas en un diagram.

Cada forma en un diagram tiene una identificación y un nombre. El ID es importante al programar con Visio: es el método principal para acceder a una forma. Cada forma también retiene información sobre de qué maestro (plantilla) está hecha.

 A[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) es un objeto en un dibujo Visio. La propiedad Shapes, expuesta por la clase Page, admite una colección de objetos Aspose.Diagram.Shape. La propiedad Shapes se puede utilizar para recuperar información sobre una forma.

En la ventana de la consola a continuación, por ejemplo, puede ver la salida de información para un diagram que contenía cuatro formas: dos terminadores, un proceso y un conector dinámico. Cada uno tiene una identificación única, así como el nombre de la forma maestra (plantilla).

|**Una ventana de consola que muestra información de forma**|
|:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_3.png)|
Para recuperar la información de la página Visio:

1. Carga un diagram.
1. Configura un bucle foreach para recorrer todas las formas en el diagram.
1. Muestra información de forma.
### **Recuperar muestra de programación**
El siguiente fragmento de código recupera la información de la forma de un Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");

foreach (Aspose.Diagram.Shape shape in vsdDiagram.Pages[0].Shapes)
{
    // Display information about the shapes
    Console.WriteLine("\nShape ID : " + shape.ID);
    Console.WriteLine("Name : " + shape.Name);
    Console.WriteLine("Master Shape : " + shape.Master.Name);
}

{{< /highlight >}}

## **Copie formas de un Visio existente**
Aspose.Diagram for .NET API permite a los desarrolladores copiar formas de la página de origen Visio a la nueva página Visio diagram. También admite la copia de formas de grupos. Este artículo describe cómo copiar todas las formas desde la página fuente diagram.

Para copiar formas, los desarrolladores también deben copiar los temas de origen PageSheet y origen Visio para conservar el estilo de relleno de forma y otras propiedades de formato.

Este ejemplo funciona de la siguiente manera:

1. Cargue una fuente Visio.
1. Inicializar un nuevo Visio
1. Agregue maestros y temas de la fuente Visio.
1. Obtenga la página de la fuente Visio.
1. Copie su hoja de página en la nueva página Visio.
1. Iterar a través de las formas de la página fuente Visio.
1. Establezca su nueva identificación y agréguela a la nueva página Visio.
1. Guarde el nuevo Visio en el almacenamiento local.
### **Ejemplo de programación de copias**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
            
// Load a source Visio
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");
            
// Initialize a new Visio
Diagram newDiagram = new Diagram();

// Add all masters from the source Visio diagram
MasterCollection originalMasters = srcVisio.Masters;
foreach (Master master in originalMasters)
    newDiagram.AddMaster(srcVisio, master.Name);

// Get the page object from the original diagram
Aspose.Diagram.Page SrcPage = srcVisio.Pages.GetPage("Page-1");
// Copy themes from the source diagram
newDiagram.CopyTheme(srcVisio);
// Copy pagesheet of the source Visio page
newDiagram.Pages[0].PageSheet.Copy(SrcPage.PageSheet);

// Copy shapes from the source Visio page
foreach (Aspose.Diagram.Shape shape in SrcPage.Shapes)
{
    newDiagram.Pages[0].Shapes.Add(shape);
}
// Save the new Visio
newDiagram.Save(dataDir + "CopyShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Copie una forma Visio en otra instancia de forma**
El método Copy de la clase Shape toma una instancia de forma para clonar.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.Copy(diagram.Pages[0].Shapes[0]);

newShape.ID = 3;

newShape.XForm.PinX.Value = 1;

newShape.XForm.PinY.Value = 1;

{{< /highlight >}}
## **Lectura de datos de forma Visio**
 La colección Props expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) la clase apoya la[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) objeto. La propiedad se puede utilizar para leer los datos de una forma (propiedades personalizadas).
### **Leer todas las propiedades de forma**
Para identificar propiedades personalizadas en Microsoft Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Datos** , después**Datos de forma** del menú.
 Todas las propiedades existentes se enumeran en el cuadro de diálogo.

|**Los datos de una forma, como se ve en Microsoft Visio.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Una ventana de consola que muestra la salida de datos de forma.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Leer muestra de programación**
Los fragmentos de código a continuación leen datos de formas (propiedades personalizadas).


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        foreach (Prop property in shape.Props)
        {
            Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
        }
        break;
    }
}

{{< /highlight >}}

### **Leer una propiedad de forma por nombre**
El fragmento de código siguiente lee una propiedad de forma por nombre (propiedad personalizada).
#### **Ejemplo de programación de lectura por nombre**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process1")
    {
        Prop property = shape.Props.GetProp("Name1");
        Console.WriteLine(property.Label.Value + ": " + property.Value.Val);
    }
}

{{< /highlight >}}

### **Read InheritAccesorios de forma**
El fragmento de código a continuación lee InheritProps de una forma.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    foreach (Aspose.Diagram.Prop prop in shape.InheritProps)
    {
        Console.WriteLine(prop.Name);
        Console.WriteLine(prop.Label.Value);
        Console.WriteLine(prop.Prompt.Value);
        Console.WriteLine(prop.Type.Value.ToString());
        Console.WriteLine(prop.Value.Val);
        Console.WriteLine(prop.Format.Value);
    }
}

{{< /highlight >}}

## **Agregar y conectar Visio Formas**
 Aspose.Diagram for .NET le permite agregar formas personalizadas y conectarlas en[diagramas que creas](https://products.aspose.com/diagram/net/).
### **Agregar y conectar formas**
El código de los ejemplos siguientes muestra cómo:

1. Crea un diagram.
1. Agregue y personalice formas (rectángulo, estrella, hexágono).
1. Conecta las formas de estrella y hexágono al rectángulo.
1. Guarda el diagram.
#### **Ejemplo de programación de adición y conexión de formas**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_TechnicalArticles();

// Set license (you can add 10 shapes without setting a license)
// License lic = new License();
// Lic.SetLicense(dataDir + "Aspose.Total.lic");

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "AddConnectShapes.vss";

// Names of the masters present in the stencil
string rectangleMaster = @"Rectangle", starMaster = @"Star 7",
    hexagonMaster = @"Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.AddShape(
    pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));
shape.Name = "Rectangle1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "7";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "1";
shape.Fill.FillForegnd.Value = "3";
shape.Fill.FillPattern.Value = 31;

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.AddShape(
    pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(starId);
shape.Text.Value.Add(new Txt(@"Star text."));
shape.Name = "Star1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineColor.Value = "#ff0000";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillBkgnd.Value = "#ff00ff";
shape.Fill.FillForegnd.Value = "#0000ff";
shape.Fill.FillPattern.Value = 31;

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.AddShape(
    pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.Pages[pageNumber].Shapes.GetShape(hexagonId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));
shape.Name = "Hexagon1";
shape.XForm.LocPinX.Ufe.F = "Width*0.5";
shape.XForm.LocPinY.Ufe.F = "Height*0.5";
shape.Line.LineWeight.Value = 0.03;
shape.Fill.FillPattern.Value = 31;

// Add master to dynamic connector from the stencil
diagram.AddMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    starId, ConnectionPointPlace.Top, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);
diagram.Pages[0].ConnectShapesViaConnector(rectangleId, ConnectionPointPlace.Bottom,
    hexagonId, ConnectionPointPlace.Left, connecter2Id);

// Save the diagram
diagram.Save(dataDir + "AddConnectShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Usar índices de conexión para conectar formas**
Aspose.Diagram for .NET API ya permite a los desarrolladores agregar nuevos puntos de conexión en la forma, y los desarrolladores ahora pueden conectar formas mediante índices de conexión.
### **Usar índices de conexión para conectar formas**
El miembro ConnectShapesViaConnectorIndex expuesto por el[Página](https://reference.aspose.com/diagram/net/aspose.diagram/page)La clase se puede usar para conectar formas usando índices de conexión. El siguiente código muestra cómo conectar formas:

1. Inicializar un nuevo dibujo.
1. Coloca cuatro formas rectangulares.
1. Agregue dos puntos de conexión adicionales, de modo que haya tres puntos de conexión en la línea del borde inferior
1. Conecte la primera forma de cada conexión inferior a otras tres formas rectangulares desde la parte superior con conectores dinámicos
1. Guardar dibujo
#### **Use índices de conexión para conectar formas Ejemplo de programación**
Use el siguiente código en su aplicación .NET para conectar formas usando índices de conexión con Aspose.Diagram for .NET API.

**C#**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Aspose.Diagram.Page page = diagram.Pages[0];

// add masters

string connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", rectangle);

diagram.AddMaster(@"C:\temp\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.AddShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.AddShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.AddShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.AddShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Aspose.Diagram.Shape shape1 = page.Shapes.GetShape(shape1_ID);

Aspose.Diagram.Shape shape2 = page.Shapes.GetShape(shape2_ID);

Aspose.Diagram.Shape shape3 = page.Shapes.GetShape(shape3_ID);

Aspose.Diagram.Shape shape4 = page.Shapes.GetShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.X.Ufe.F = "Width*0.33";

connection1.Y.Ufe.F = "Height*0";

Connection connection3 = new Connection();

connection3.X.Ufe.F = "Width*0.66";

connection3.Y.Ufe.F = "Height*0";

shape1.Connections.Add(connection1);

shape1.Connections.Add(connection3);



// add connector shapes

Aspose.Diagram.Shape connector1 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector2 = new Aspose.Diagram.Shape();

Aspose.Diagram.Shape connector3 = new Aspose.Diagram.Shape();

long connecter1Id = diagram.AddShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.AddShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.AddShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.ConnectShapesViaConnectorIndex(shape1.ID, 6, shape2.ID, 3, connecter1Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 1, shape3.ID, 3, connecter2Id);

page.ConnectShapesViaConnectorIndex(shape1.ID, 7, shape4.ID, 3, connecter3Id);

// save drawing

diagram.Save(@"C:\temp\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Recuperar la forma principal de una subforma**
Aspose.Diagram for .NET permite a los desarrolladores recuperar la forma principal de una subforma.
### **Obtener la forma principal**
los[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)La clase ofrece la propiedad ParentShape para recuperar la forma principal.
#### **Obtenga la muestra de programación de formas principales**

{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Shape parentShape = shape.ParentShape;
Console.WriteLine("Parent Shape's Properties:");
Console.WriteLine("Shape ID: " + parentShape.ID);
Console.WriteLine("Shape Name: " + parentShape.Name);
Console.WriteLine("Shape Type: " + parentShape.Type);
{{< /highlight >}}

