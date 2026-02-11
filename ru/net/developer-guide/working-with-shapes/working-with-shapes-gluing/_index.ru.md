---
title: Работа со склеиванием фигур
type: docs
weight: 40
url: /ru/net/working-with-shapes-gluing/
description: В этом разделе объясняется, как получить фигуры, которые приклеиваются к определенной фигуре с помощью Aspose.Diagram.
---
## **Приклейте соединители к определенной форме**
[Добавить и соединить Visio фигуры](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for .NET. Также можно найти соединители, приклеенные к этой фигуре.
### **Получение склеенных фигур**
 Метод GluedShapes, предоставленный[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)можно использовать для получения списка идентификаторов всех соединителей, приклеенных к фигуре, или, если рассматриваемая фигура является соединителем, идентификаторы фигур, к которым он подключен.[Коллекция форм](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите список идентификаторов всех соединителей, приклеенных к этой фигуре.
#### **Пример программирования Get Connectors Glued**
Используйте следующий код в своем приложении .NET, чтобы найти все соединители, приклеенные к фигуре, используя Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// Get shape by an ID
Shape shape = diagram.Pages[0].Shapes.GetShape(90);
// Get all glued 1D shapes
long[] gluedShapeIds = shape.GluedShapes(GluedShapesFlags.GluedShapesAll1D, null, null);

// Display shape ID and name
foreach (long id in gluedShapeIds)
{
    shape = diagram.Pages[0].Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}
```
## **Склейте Visio формы вместе с точкой соединения**
Aspose.Diagram for .NET позволяет разработчикам склеивать фигуры вместе через точки соединения.
### **Клеевые формы**
 Метод GlueShapes, предоставленный[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_1.png)</p>|<p>**diagram после склеивания фигур** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Клеевые фигуры.
1. Сохранить diagram.
#### **Glue Visio Образец программирования фигур**
Используйте следующий код в своем приложении .NET, чтобы склеить фигуры через точки соединения:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");
// Set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.GlueShapes(shape1_ID, Aspose.Diagram.Manipulation.ConnectionPointPlace.Center, shape2_ID);

// Save diagram
diagram.Save(dataDir + "GlueVisioShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Приклейте фигуры внутри контейнера**
Aspose.Diagram for .NET позволяет разработчикам склеивать групповые фигуры внутри контейнера.
### **Форма группы клея**
 Метод GlueShapesInContainer, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_3.png)</p>|<p>**diagram после склеивания групповых форм** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Склеиваем фигурки групп.
1. Сохранить diagram.
#### **Склеивание фигур внутри примера программирования**
Используйте следующий код в своем приложении .NET, чтобы склеить фигуру группы внутри контейнера:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.GlueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// Page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.Save(dataDir + "GlueContainerShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
