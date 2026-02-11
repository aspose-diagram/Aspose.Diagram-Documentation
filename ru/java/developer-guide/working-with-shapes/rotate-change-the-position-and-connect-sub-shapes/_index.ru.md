---
title: Вращение, изменение положения и соединение подформ
type: docs
weight: 60
url: /ru/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Повернуть фигуру на подходящий угол**
 Aspose.Diagram for Java позволяет поворачивать фигуру под любым углом. Метод SetAngle, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) можно использовать для поворота фигуры на любой желаемый угол. Он принимает один параметр в качестве угла.
### **Поворот образца программирования формы**
Используйте следующий код в своем приложении Java, чтобы повернуть фигуру с помощью Aspose.Diagram for Java.


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

## **Изменить положение фигуры**
Класс Shape позволяет изменить положение фигуры. Соединительная линия автоматически настраивается, когда фигура перемещается в другое положение.

Методы Move и MoveTo, предоставляемые классом Shape, поддерживают изменение положения фигуры как части группы или нет.
Примеры кода в этой статье перемещают фигуру на странице.
**Ввод diagram** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/cThgWnB.png)


**diagram после перемещения формы** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/Q3QByqe.png)

Процесс перемещения фигуры:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Переместить фигуру в другое место
1. Сохраните номер diagram.
### **Пример программирования изменения позиции**
Фрагмент кода ниже показывает, как переместить фигуру. Код извлекает страницу Visio по имени и форме по идентификатору 16 и перемещает ее позицию.


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

## **Соедините подформы групп**
В этом разделе подробно описывается, как соединить два подфигуры двух разных форм групп на диаграммах Microsoft Visio с использованием Aspose.Diagram for Java.

 Метод ConnectShapesViaConnector, предоставляемый[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) можно использовать для соединения фигур по их идентификаторам. Метод AddShape, представленный[Diagram](https://reference.aspose.com/diagram/java)class, можно использовать для добавления формы.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/74rDby5.png)</p>|<p>**diagram после соединения подформ** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной странице.
1. Добавьте форму динамического соединителя на выбранную страницу.
1. Подключить подформы
### **Образец программирования Connect Sub-Shapes**
Используйте следующий код в своем приложении Java, чтобы соединить подформы двух разных фигур группы, используя Aspose.Diagram for Java.


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

## **Соедините фигуры с определенной фигурой**
[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for Java. Также можно найти фигуры, которые связаны с определенной фигурой.

 Метод ConnectedShapes, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) можно использовать для получения идентификаторов фигур, связанных с фигурой. Метод GetShape, представленный[Коллекция форм](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите имена всех фигур, связанных с выбранной фигурой.
### **Получить пример программирования фигур**
Используйте следующий код в своем приложении Java, чтобы найти все фигуры, связанные с определенной фигурой, используя Aspose.Diagram for Java.


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

