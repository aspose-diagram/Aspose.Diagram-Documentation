---
title: Используйте индексы соединения для соединения фигур
type: docs
weight: 20
url: /ru/java/use-connection-indexes-to-connect-shapes/
---
## **Добавьте новые соединения в фигуру и используйте индексы соединений для соединения фигур.**
Aspose.Diagram for Java API помогает разработчикам добавлять новые точки соединения на фигуру, и теперь разработчики могут соединять фигуры с помощью индексов соединения.
### **Используйте индексы соединения для соединения фигур**
Элемент connectShapesViaConnectorIndex, предоставляемый[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)класс можно использовать для соединения фигур с помощью индексов соединения. В следующем коде показано, как соединить фигуры:

1. Инициализировать новый рисунок.
1. Поместите четыре прямоугольника
1. Добавьте две дополнительные точки соединения, чтобы на нижней линии границы было три точки соединения.
1. Соедините первую фигуру от каждого нижнего соединения с тремя другими прямоугольными фигурами сверху с помощью динамических соединителей.
1. Сохранить рисунок
#### **использовать индексы соединения для соединения фигур Образец программирования**
Используйте следующий код в своем приложении Java, чтобы соединить фигуры с индексами соединения с Aspose.Diagram for Java API.

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

connection1.setIX(shape1.getConnections().add(connection1));

connection3.setIX( shape1.getConnections().add(connection3));

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


// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
