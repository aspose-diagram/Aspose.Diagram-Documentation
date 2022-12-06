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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-AddingNewShape-AddingNewShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CopyShape-CopyShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadAllShapeProps-ReadAllShapeProps.cs" >}}
### **Чтение свойства формы по имени**
Фрагмент кода ниже считывает свойство фигуры по имени (настраиваемое свойство).
#### **Пример программирования чтения по имени**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ReadShapePropByName-ReadShapePropByName.cs" >}}
### **Чтение InheritProps формы**
Фрагмент кода ниже читает InheritProps формы.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-InheritProps-InheritProps.cs" >}}
## **Добавить и соединить Visio фигуры**
 Aspose.Diagram for .NET позволяет добавлять индивидуальные формы и соединять их в[диаграммы, которые вы создаете](https://products.aspose.com/diagram/net/).
### **Добавление и соединение фигур**
Код в приведенных ниже примерах показывает, как:

1. Создайте номер diagram.
1. Добавляйте и настраивайте фигуры (прямоугольник, звезда, шестиугольник).
1. Соедините фигуры звезды и шестиугольника с прямоугольником.
1. Сохраните номер diagram.
#### **Пример программирования добавления и соединения фигур**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Technical-Articles-AddConnectShapes-AddConnectShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.cs" >}}
