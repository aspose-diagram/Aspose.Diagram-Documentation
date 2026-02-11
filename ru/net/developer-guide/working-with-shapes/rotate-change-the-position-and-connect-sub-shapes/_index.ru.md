---
title: Вращение, изменение положения и соединение подформ
type: docs
weight: 30
url: /ru/net/rotate-change-the-position-and-connect-sub-shapes/
description: В этом разделе объясняется, как повернуть фигуру visio с помощью Aspose.Diagram.
---
## **Повернуть фигуру на подходящий угол**
 Aspose.Diagram for .NET позволяет поворачивать фигуру под любым углом. Метод SetAngle, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) можно использовать для поворота фигуры на любой желаемый угол. Он принимает один параметр в качестве угла.
### **Поворот образца программирования формы**
Используйте следующий код в своем приложении .NET, чтобы повернуть фигуру с помощью Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);

// Add a shape and set the angle
shape.SetAngle(190);

// Save diagram
diagram.Save(dataDir + "RotateVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Изменить положение фигуры**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Класс позволяет изменить положение фигуры. Соединительная линия автоматически настраивается, когда фигура перемещается в другое положение. Методы Move и MoveTo, предоставляемые[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, поддерживают изменение положения фигуры как части группы или нет. Примеры кода в этой статье перемещают фигуру на странице.

Процесс перемещения фигуры:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Переместить фигуру в другое место
1. Сохраните номер diagram.
### **Пример программирования изменения позиции**
Фрагмент кода ниже показывает, как переместить фигуру. Код извлекает страницу Visio по имени и форме по идентификатору 16 и перемещает ее позицию.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");
// Get shape by id
Shape shape = page.Shapes.GetShape(16);
// Move shape from its position, it adds values in coordinates
shape.Move(1, 1);

// Save diagram
diagram.Save(dataDir + "MoveVisioShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Соедините подформы групп**
 В этом разделе подробно описывается, как соединить два подфигуры двух разных групповых фигур на диаграммах Microsoft Visio с помощью Aspose.Diagram for .NET. Метод ConnectShapesViaConnector, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать для соединения фигур по их идентификаторам. Метод AddShape, представленный[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class, можно использовать для добавления формы.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной странице.
1. Добавьте форму динамического соединителя на выбранную страницу.
1. Подключить подформы
### **Образец программирования Connect Sub-Shapes**
Используйте следующий код в своем приложении .NET, чтобы соединить подформы двух разных фигур группы, используя Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Access a particular page
Page page = diagram.Pages.GetPage("Page-3");
           
// Initialize connector shape
Shape shape = new Shape();
shape.Line.EndArrow.Value = 4;
shape.Line.LineWeight.Value = 0.01388;

// Add shape
long connecter1Id = diagram.AddShape(shape, "Dynamic connector", page.ID);
// Connect sub-shapes
page.ConnectShapesViaConnector(shapeFromId, ConnectionPointPlace.Right, shapeToId, ConnectionPointPlace.Left, connecter1Id);
// Save Visio drawing
diagram.Save(dataDir + "ConnectVisioSubShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Соедините фигуры с определенной фигурой**
[Добавить и соединить Visio фигуры](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for .NET. Также можно найти фигуры, которые связаны с определенной фигурой.

 Метод ConnectedShapes, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) можно использовать для получения идентификаторов фигур, связанных с фигурой. Метод GetShape, представленный[Коллекция форм](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите имена всех фигур, связанных с выбранной фигурой.
### **Получить пример программирования фигур**
Используйте следующий код в своем приложении .NET, чтобы найти все фигуры, связанные с определенной фигурой, используя Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get shape by id
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(16);
// Get connected shapes
long[] connectedShapeIds = shape.ConnectedShapes(ConnectedShapesFlags.ConnectedShapesAllNodes, null);

foreach (long id in connectedShapeIds)
{
    shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(id);
    Console.WriteLine("ID: " + shape.ID + "\t\t Name: " + shape.Name);
}

{{< /highlight >}}
```
