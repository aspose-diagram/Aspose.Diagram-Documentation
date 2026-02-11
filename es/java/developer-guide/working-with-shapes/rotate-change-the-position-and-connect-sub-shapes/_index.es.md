---
title: Rotar, cambiar la posición y conectar subformas
type: docs
weight: 60
url: /es/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Girar una forma con ángulo adecuado**
 Aspose.Diagram for Java le permite girar una forma en cualquier ángulo. El método SetAngle expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase se puede usar para rotar una forma a cualquier ángulo deseado. Toma un solo parámetro como un ángulo.
### **Rotar una muestra de programación de forma**
Use el siguiente código en su aplicación Java para rotar una forma usando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Cambiar la posición de una forma**
La clase de forma le permite cambiar la posición de una forma. La línea conectora se ajusta automáticamente cuando la forma se mueve a una posición diferente.

Los métodos Move y MoveTo, expuestos por la clase Shape, admiten cambiar la posición de una forma como parte de un grupo o no.
Los ejemplos de código de este artículo mueven una forma en la página.
**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/cThgWnB.png)


**El diagram después de mover la forma.** 

![todo:imagen_alternativa_texto](http://i.imgur.com/Q3QByqe.png)

El proceso para mover una forma es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Mover forma a una ubicación diferente
1. Guarda el diagram.
### **Ejemplo de programación de cambio de posición**
El fragmento de código siguiente muestra cómo mover la forma. El código recupera una página Visio por nombre y forma por ID 16 y mueve su posición.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Conectar subformas de los grupos**
Este tema explica cómo conectar dos subformas de dos formas de grupo diferentes en diagramas Microsoft Visio usando Aspose.Diagram for Java.

 El método ConnectShapesViaConnector expuesto por el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) La clase se puede usar para conectar las formas por sus ID. El método AddShape, expuesto por el[Diagram](https://reference.aspose.com/diagram/java)clase, se puede utilizar para agregar una forma.

|<p>**La entrada diagram** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/74rDby5.png)</p>|<p>**El diagram después de la conexión de subformas** </p><p>![todo:imagen_alternativa_texto](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una página en particular.
1. Agregue forma de conector dinámico a la página seleccionada.
1. Conectar subformas
### **Ejemplo de programación de Connect Sub-shapes**
Use el siguiente código en su aplicación Java para conectar las subformas de dos formas de grupos diferentes usando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Obtener las formas conectadas a una forma particular**
[Agregar y conectar Visio Formas](/diagram/es/java/add-and-connect-visio-shapes/) explica cómo agregar una forma y conectarla a otras formas en diagramas Microsoft Visio usando Aspose.Diagram for Java. También es posible encontrar formas que están conectadas a una forma específica.

 El método ConnectedShapes expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) La clase se puede usar para obtener los ID de las formas conectadas a una forma. El método GetShape, expuesto por el[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, se puede usar para encontrar una forma por su ID.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Obtenga los nombres de todas las formas conectadas a la forma seleccionada.
### **Obtener muestra de programación de formas**
Use el siguiente código en su aplicación Java para encontrar todas las formas conectadas a una forma específica usando Aspose.Diagram for Java.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

