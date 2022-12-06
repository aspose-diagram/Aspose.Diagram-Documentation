---
title: Используйте индексы соединения для соединения фигур
type: docs
weight: 10
url: /ru/net/use-connection-indexes-to-connect-shapes/
---
## **Добавьте новые соединения в фигуру и используйте индексы соединений для соединения фигур.**
Aspose.Diagram for .NET API уже позволяет разработчикам добавлять новые точки соединения на фигуру, и теперь разработчики могут соединять фигуры с помощью индексов соединения.
### **Используйте индексы соединения для соединения фигур**
Элемент ConnectShapesViaConnectorIndex, предоставляемый[Страница](https://reference.aspose.com/diagram/net/aspose.diagram/page)класс можно использовать для соединения фигур с помощью индексов соединения. В следующем коде показано, как соединить фигуры:

1. Инициализировать новый рисунок.
1. Поместите четыре прямоугольника
1. Добавьте две дополнительные точки соединения, чтобы на нижней линии границы было три точки соединения.
1. Соедините первую фигуру от каждого нижнего соединения с тремя другими прямоугольными фигурами сверху с помощью динамических соединителей.
1. Сохранить рисунок
#### **использовать индексы соединения для соединения фигур Образец программирования**
Используйте следующий код в своем приложении .NET для соединения фигур с помощью индексов соединения с Aspose.Diagram for .NET API.

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
