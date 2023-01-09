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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-AddingNewShape-AddingNewShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CopyShape-CopyShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadAllShapeProps-ReadAllShapeProps.cs" >}}
### **Leer una propiedad de forma por nombre**
El fragmento de código siguiente lee una propiedad de forma por nombre (propiedad personalizada).
#### **Ejemplo de programación de lectura por nombre**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadShapePropByName-ReadShapePropByName.cs" >}}
### **Read InheritAccesorios de forma**
El fragmento de código a continuación lee InheritProps de una forma.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-InheritProps-InheritProps.cs" >}}
## **Agregar y conectar Visio Formas**
 Aspose.Diagram for .NET le permite agregar formas personalizadas y conectarlas en[diagramas que creas](https://products.aspose.com/diagram/net/).
### **Agregar y conectar formas**
El código de los ejemplos siguientes muestra cómo:

1. Crea un diagram.
1. Agregue y personalice formas (rectángulo, estrella, hexágono).
1. Conecta las formas de estrella y hexágono al rectángulo.
1. Guarda el diagram.
#### **Ejemplo de programación de adición y conexión de formas**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Technical-Articles-AddConnectShapes-AddConnectShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.cs" >}}
