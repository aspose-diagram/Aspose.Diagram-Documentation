---
title: Добавление, извлечение, копирование и чтение данных формы Visio
type: docs
weight: 10
url: /ru/net/add-retrieve-copy-and-read-visio-shape-data/
description: В этом разделе объясняется, как добавить фигуру, установить свойство фигуры или скопировать фигуру с помощью Aspose.Diagram.
---
## **Добавление новой формы в Visio**
Aspose.Diagram for .NET позволяет вам управлять Microsoft Visio диаграммами различными способами. Одна из вещей, которую вы можете сделать, это добавить новые фигуры на диаграммы. Aspose.Diagram for .NET позволяет добавить новую форму к diagram. Добавленную форму также можно настроить с помощью Aspose.Diagram for .NET.

В этом разделе описывается, как добавить новую прямоугольную фигуру в файл diagram.

Используйте Aspose.Diagram for .NET API для создания новых фигур, а затем добавьте эти фигуры в коллекцию фигур diagram.

Чтобы добавить новую форму:

1. **Найдите страницу** - Каждый Visio diagram содержит набор страниц. Разработчики могут получить страницу по идентификатору страницы или имени и сохранить нужную страницу в[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)объект класса.
1. **Добавьте требуемый мастер формы** - Каждый Visio diagram содержит коллекцию мастеров. Разработчики могут добавить мастер (по идентификатору или имени) из существующего файла трафарета (по прямому пути или файловому потоку).
1. **Добавить форму в Visio diagram** - Разработчики могут разместить новую фигуру в Visio diagram по индексу страницы (начиная с 0), главному имени, PinX, PinY, высоте (необязательно) и ширине (необязательно).
1. **Установить свойства формы** - Метод AddShape класса Diagram возвращает идентификатор формы. Разработчики могут получить форму из Visio diagram, используя этот идентификатор, а затем установить ее свойства, например цвет, положение, выравнивание и текст.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](add-retrieve-copy-and-read-visio-shape-data_1.png)</p>|<p>**diagram с добавленной формой** </p><p>![дело:изображение_альтернативный_текст](add-retrieve-copy-and-read-visio-shape-data_2.png)</p>|
|:- |:- |
### **Добавить пример программирования**
Фрагмент кода ниже показывает, как выполнить каждый шаг.


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

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
## **Получение информации о форме**
[Работа с диаграммами](/diagram/ru/net/working-with-diagrams/)объясняет, как создавать диаграммы, добавлять фигуры и соединители, а затем как получать информацию о diagram элементах, таких как[страницы](/diagram/ru/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [мастера](https://docs.aspose.com/diagram/net/working-with-masters/), [соединители](/diagram/ru/net/retrieving-connector-information/) а также[шрифты](/diagram/ru/net/retrieving-font-information/). В этой статье рассматривается, как получить информацию о фигурах в файле diagram.

Каждая фигура в diagram имеет идентификатор и имя. Идентификатор важен при программировании с помощью Visio: это основной метод доступа к фигуре. Каждая фигура также сохраняет информацию о том, из какого шаблона (трафарета) она сделана.

 А[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) является объектом на чертеже Visio. Свойство Shapes, предоставляемое классом Page, поддерживает коллекцию объектов Aspose.Diagram.Shape. Свойство Shapes можно использовать для получения информации о фигуре.

Например, в окне консоли ниже вы можете увидеть вывод информации для diagram, который содержит четыре фигуры: два терминатора, процесс и динамический коннектор. У каждого есть уникальный идентификатор, а также имя основной формы (трафарета).

|**Окно консоли с информацией о форме**|
|:- |
|![дело:изображение_альтернативный_текст](add-retrieve-copy-and-read-visio-shape-data_3.png)|
Чтобы получить информацию о странице Visio:

1. Загружает diagram.
1. Настраивает цикл foreach для перебора всех фигур в diagram.
1. Отображает информацию о форме.
### **Получить пример программирования**
Следующий фрагмент кода извлекает информацию о форме из Visio diagram.


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

## **Копирование фигур из существующей Visio**
Aspose.Diagram for .NET API позволяет разработчикам копировать фигуры с исходной страницы Visio на новую страницу Visio diagram. Он также поддерживает копирование групповых фигур. В этой статье описывается, как скопировать все фигуры с исходной страницы diagram.

Чтобы скопировать фигуры, разработчикам также следует скопировать исходные темы PageSheet и исходные темы Visio, чтобы сохранить стиль заливки фигур и другие свойства форматирования.

Этот пример работает следующим образом:

1. Загрузите источник Visio.
1. Инициализировать новый Visio
1. Добавляйте мастера и темы из источника Visio.
1. Получить страницу из источника Visio.
1. Скопируйте его PageSheet на новую страницу Visio.
1. Переберите формы исходной страницы Visio.
1. Установите его новый идентификатор и добавьте на новую страницу Visio.
1. Сохраните новый Visio в локальном хранилище.
### **Копировать пример программирования**

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

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
## **Скопируйте фигуру Visio в другой экземпляр фигуры.**
Метод Copy класса Shape использует экземпляр формы для клонирования.

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
## **Чтение данных формы Visio**
 Коллекция Props, предоставленная[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс поддерживает[Aspose.Diagram.Prop](http://www.aspose.com/api/net/diagram/aspose.diagram/prop) объект. Свойство можно использовать для чтения данных фигуры (настраиваемые свойства).
### **Чтение всех свойств формы**
Чтобы определить пользовательские свойства в Microsoft Visio:

1. В diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Данные** , тогда**Данные формы** из меню.
 Все существующие свойства перечислены в диалоговом окне.

|**Данные фигуры, как показано в Microsoft Visio.**|** |
|:- |:- |
|![дело:изображение_альтернативный_текст](add-retrieve-copy-and-read-visio-shape-data_4.png)||


|**Окно консоли, показывающее выходные данные формы.**|** |
|:- |:- |
|![дело:изображение_альтернативный_текст](add-retrieve-copy-and-read-visio-shape-data_5.png)||
#### **Читать пример программирования**
Фрагменты кода ниже считывают данные формы (настраиваемые свойства).


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

### **Чтение свойства формы по имени**
Фрагмент кода ниже считывает свойство фигуры по имени (настраиваемое свойство).
#### **Пример программирования чтения по имени**

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

### **Чтение InheritProps формы**
Фрагмент кода ниже читает InheritProps формы.


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

## **Добавить и соединить Visio фигуры**
 Aspose.Diagram for .NET позволяет добавлять индивидуальные формы и соединять их в[диаграммы, которые вы создаете](https://products.aspose.com/diagram/net/).
### **Добавление и соединение фигур**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Добавляйте и настраивайте фигуры (прямоугольник, звезда, шестиугольник).
1. Соедините фигуры звезды и шестиугольника с прямоугольником.
1. Сохраните номер diagram.
#### **Пример программирования добавления и соединения фигур**

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

## **Используйте индексы соединения для соединения фигур**
Aspose.Diagram for .NET API уже позволяет разработчикам добавлять новые точки соединения на фигуру, и теперь разработчики могут соединять фигуры с помощью индексов соединения.
### **Используйте индексы соединения для соединения фигур**
Элемент ConnectShapesViaConnectorIndex, предоставляемый[Страница](https://reference.aspose.com/diagram/net/aspose.diagram/page)класс можно использовать для соединения фигур с помощью индексов соединения. В следующем коде показано, как соединить фигуры:

1. Инициализировать новый рисунок.
1. Поместите четыре прямоугольника
1. Добавьте две дополнительные точки соединения, чтобы на нижней линии границы было три точки соединения.
1. Соедините первую фигуру от каждого нижнего соединения с тремя другими прямоугольными фигурами сверху с помощью динамических соединителей.
1. Сохранить рисунок
#### **Использование индексов соединения для соединения фигур Образец программирования**
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
## **Получить родительскую форму подформы**
Aspose.Diagram for .NET позволяет разработчикам извлекать родительскую форму подформы.
### **Получить родительскую форму**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)класс предлагает свойство ParentShape для получения родительской формы.
#### **Получить пример программирования родительской фигуры**

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

