---
title: Trabajar con datos de forma Visio
type: docs
weight: 30
url: /es/java/working-with-visio-shape-data/
---
## **Agregar una nueva forma en Visio**
Aspose.Diagram for Java le permite manipular Microsoft Visio diagramas de diferentes maneras. Una de las cosas que puede hacer es agregar nuevas formas a los diagramas. Aspose.Diagram for Java le permite agregar una nueva forma a un diagram. La forma agregada también se puede personalizar usando Aspose.Diagram for Java.

Este tema describe cómo agregar una nueva forma de rectángulo a un diagram.

Use Aspose.Diagram for Java's API para crear nuevas formas y luego agregue estas formas a la colección de formas de diagram.

Para agregar una nueva forma:

1. **Encuentra la página** - Cada Visio diagram contiene una colección de páginas. Los desarrolladores pueden recuperar la página por ID o nombre de página y almacenar la página requerida en el[Página](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)objeto de clase.
1. **Agregue el maestro requerido de una forma** - Cada Visio diagram contiene una colección de maestros. Los desarrolladores pueden agregar un maestro (por ID o nombre) del archivo de plantilla existente (por ruta directa o flujo de archivo).
1. **Añadir forma en el Visio diagram** - Los desarrolladores pueden colocar una nueva forma en el Visio diagram por índice de página (a partir de 0), nombre maestro, PinX, PinY, alto (opcional) y ancho (opcional).
1. **Establecer propiedades de forma** - El método AddShape de la clase Diagram devuelve el ID de la forma. Los desarrolladores pueden recuperar la forma de un Visio diagram usando este ID y luego establecer sus propiedades, por ejemplo, color, posición, alineación y texto.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](working-with-visio-shape-data_1.png)</p>|<p>**El diagram con una forma añadida** </p><p>![todo:imagen_alternativa_texto](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Agregar muestra de programación**
El fragmento de código a continuación muestra cómo hacer cada paso.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Recuperación de información de forma**
[Trabajar con diagramas](/diagram/es/java/working-with-diagrams/)explica cómo crear diagramas, agregar formas y conectores, y luego cómo recuperar información sobre diagram elementos como[paginas](/diagram/es/java/retrieve-get-copy-and-insert-a-page/), [maestros](/diagram/es/java/working-with-masters/) , conectores y[fuentes](/diagram/es/java/aspose-diagram-font-operations/). Este artículo analiza cómo recuperar información sobre formas en un diagram.

Cada forma en un diagram tiene una identificación y un nombre. El ID es importante al programar con Visio: es el método principal para acceder a una forma. Cada forma también retiene información sobre de qué maestro (plantilla) está hecha.

 A[Forma](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) es un objeto en un dibujo Visio. La propiedad Shapes, expuesta por la clase Page, admite una colección de objetos Aspose.Diagram.Shape. La propiedad Shapes se puede utilizar para recuperar información sobre una forma.

En la ventana de la consola a continuación, por ejemplo, puede ver la salida de información para un diagram que contenía cuatro formas: dos terminadores, un proceso y un conector dinámico. Cada uno tiene una identificación única, así como el nombre de la forma maestra (plantilla).

**Una ventana de consola que muestra información de forma**

![todo:imagen_alternativa_texto](working-with-visio-shape-data_3.png)

Para recuperar la información de la página Visio:

1. Carga un diagram.
1. Configura un bucle foreach para recorrer todas las formas en el diagram.
1. Muestra información de forma.
### **Recuperar muestra de programación**
El siguiente fragmento de código recupera la información de la forma de un Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
## **Copie formas de un Visio existente**
Aspose.Diagram for Java API permite a los desarrolladores copiar formas de la página de origen Visio a la nueva página Visio diagram. También admite la copia de formas de grupos. Este artículo describe cómo copiar todas las formas desde la página fuente diagram.

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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 Agradecemos sus consultas y sugerencias en[Aspose.Diagram Foro](https://forum.aspose.com/c/diagram/17). Responderemos a la brevedad.

{{% /alert %}}
## **Copie una forma Visio en otra instancia de forma**
El método de copia de la clase Shape toma una instancia de forma para clonar.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **Lectura de datos de forma Visio**
 La colección Props expuesta por la clase Shape admite la[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) objeto. La propiedad se puede utilizar para leer los datos de una forma (propiedades personalizadas).
### **Leer todas las propiedades de forma**
Para identificar propiedades personalizadas en Microsoft Visio:

1. En un diagram, haga clic derecho en una forma.
1.  Seleccione**Datos** , después**Datos de forma** del menú.
 Todas las propiedades existentes se enumeran en el cuadro de diálogo.

|**Los datos de una forma, como se ve en Microsoft Visio.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](http://i.imgur.com/2loM7b0.png)||


|**Una ventana de consola que muestra la salida de datos de forma.**|** |
|:- |:- |
|![todo:imagen_alternativa_texto](http://i.imgur.com/kmAKNrx.png)||
#### **Leer muestra de programación**
Los fragmentos de código a continuación leen datos de formas (propiedades personalizadas).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **Leer una propiedad de forma por nombre**
El fragmento de código siguiente lee una propiedad de forma por nombre (propiedad personalizada).
#### **Ejemplo de programación de lectura por nombre**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **Usar índices de conexión para conectar formas**
Aspose.Diagram for Java API ya permite a los desarrolladores agregar nuevos puntos de conexión en la forma, y los desarrolladores ahora pueden conectar formas mediante índices de conexión.
### **Usar índices de conexión para conectar formas**
El miembro connectShapesViaConnectorIndex expuesto por la clase Page se puede usar para conectar formas mediante índices de conexión. El siguiente código muestra cómo conectar formas:

1. Inicializar un nuevo dibujo.
1. Coloca cuatro formas rectangulares.
1. Agregue dos puntos de conexión adicionales, de modo que haya tres puntos de conexión en la línea del borde inferior
1. Conecte la primera forma de cada conexión inferior a otras tres formas rectangulares desde la parte superior con conectores dinámicos
1. Guardar dibujo
#### **Use índices de conexión para conectar formas Ejemplo de programación**
Use el siguiente código en su aplicación Java para conectar formas usando índices de conexión con Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Recuperar la forma principal de una subforma**
Aspose.Diagram for Java permite a los desarrolladores recuperar la forma principal de una subforma.
### **Obtener la forma principal**
La clase Shape ofrece la propiedad getParentShape para recuperar la forma principal.
#### **Obtenga la muestra de programación de formas principales**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
