---
title: Работа со склеиванием фигур
type: docs
weight: 10
url: /ru/java/working-with-shapes-gluing/
---
## **Приклейте соединители к определенной форме**
[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for Java. Также можно найти соединители, приклеенные к этой фигуре.
### **Получение склеенных фигур**
 Метод GluedShapes, предоставленный[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)можно использовать для получения списка идентификаторов всех соединителей, приклеенных к фигуре, или, если рассматриваемая фигура является соединителем, идентификаторы фигур, к которым он подключен.[Коллекция форм](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите список идентификаторов всех соединителей, приклеенных к этой фигуре.
#### **Пример программирования Get Connectors Glued**
Используйте следующий код в своем приложении Java, чтобы найти все соединители, приклеенные к фигуре, используя Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}
```
## **Склейте Visio формы вместе с точкой соединения**
Aspose.Diagram for Java позволяет разработчикам склеивать фигуры вместе через точки соединения.
### **Клеевые формы**
 Метод GlueShapes, предоставленный[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/Z69f4hg.png)</p>|<p>**diagram после склеивания фигур** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Клеевые фигуры.
1. Сохранить diagram.
#### **Glue Visio Образец программирования фигур**
Используйте следующий код в своем приложении Java, чтобы склеить фигуры через точки соединения:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Приклейте фигуры внутри контейнера**
Aspose.Diagram for Java позволяет разработчикам склеивать групповые фигуры внутри контейнера.
### **Форма группы клея**
Можно использовать метод GlueShapesInContainer, предоставляемый классом Page.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/HRRzIEh.png)</p>|<p>**diagram после склеивания групповых форм** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Склеиваем фигурки групп.
1. Сохранить diagram.
#### **Склеивание фигур внутри примера программирования**
Используйте следующий код в своем приложении Java, чтобы склеить фигуру группы внутри контейнера:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
