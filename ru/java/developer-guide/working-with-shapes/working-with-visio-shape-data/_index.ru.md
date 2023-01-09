﻿---
title: Работа с данными формы Visio
type: docs
weight: 30
url: /ru/java/working-with-visio-shape-data/
---
## **Добавление новой формы в Visio**
Aspose.Diagram for Java позволяет вам управлять Microsoft Visio диаграммами различными способами. Одна из вещей, которую вы можете сделать, это добавить новые фигуры на диаграммы. Aspose.Diagram for Java позволяет добавить новую форму к diagram. Добавленную форму также можно настроить с помощью Aspose.Diagram for Java.

В этом разделе описывается, как добавить новую прямоугольную фигуру в файл diagram.

Используйте Aspose.Diagram for Java API для создания новых фигур, а затем добавьте эти фигуры в коллекцию фигур diagram.

Чтобы добавить новую форму:

1. **Найдите страницу** - Каждый Visio diagram содержит набор страниц. Разработчики могут получить страницу по идентификатору страницы или имени и сохранить нужную страницу в[Страница](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)объект класса.
1. **Добавьте требуемый мастер формы** - Каждый Visio diagram содержит коллекцию мастеров. Разработчики могут добавить мастер (по идентификатору или имени) из существующего файла трафарета (по прямому пути или файловому потоку).
1. **Добавить форму в Visio diagram** - Разработчики могут разместить новую фигуру в Visio diagram по индексу страницы (начиная с 0), главному имени, PinX, PinY, высоте (необязательно) и ширине (необязательно).
1. **Установить свойства формы** - Метод AddShape класса Diagram возвращает идентификатор формы. Разработчики могут получить форму из Visio diagram, используя этот идентификатор, а затем установить ее свойства, например цвет, положение, выравнивание и текст.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](working-with-visio-shape-data_1.png)</p>|<p>**diagram с добавленной формой** </p><p>![дело:изображение_альтернативный_текст](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Добавить пример программирования**
Фрагмент кода ниже показывает, как выполнить каждый шаг.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
## **Получение информации о форме**
[Работа с диаграммами](/diagram/ru/java/working-with-diagrams/)объясняет, как создавать диаграммы, добавлять фигуры и соединители, а затем как получать информацию о diagram элементах, таких как[страницы](/diagram/ru/java/retrieve-get-copy-and-insert-a-page/), [мастера](/diagram/ru/java/working-with-masters/) , разъемы и[шрифты](/diagram/ru/java/aspose-diagram-font-operations/). В этой статье рассматривается, как получить информацию о фигурах в файле diagram.

Каждая фигура в diagram имеет идентификатор и имя. Идентификатор важен при программировании с помощью Visio: это основной метод доступа к фигуре. Каждая фигура также сохраняет информацию о том, из какого шаблона (трафарета) она сделана.

 А[Форма](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) является объектом на чертеже Visio. Свойство Shapes, предоставляемое классом Page, поддерживает коллекцию объектов Aspose.Diagram.Shape. Свойство Shapes можно использовать для получения информации о фигуре.

Например, в окне консоли ниже вы можете увидеть вывод информации для diagram, который содержит четыре фигуры: два терминатора, процесс и динамический коннектор. У каждого есть уникальный идентификатор, а также имя основной формы (трафарета).

**Окно консоли с информацией о форме**

![дело:изображение_альтернативный_текст](working-with-visio-shape-data_3.png)

Чтобы получить информацию о странице Visio:

1. Загружает diagram.
1. Настраивает цикл foreach для перебора всех фигур в diagram.
1. Отображает информацию о форме.
### **Получить пример программирования**
Следующий фрагмент кода извлекает информацию о форме из Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
## **Копирование фигур из существующей Visio**
Aspose.Diagram for Java API позволяет разработчикам копировать фигуры с исходной страницы Visio на новую страницу Visio diagram. Он также поддерживает копирование групповых фигур. В этой статье описывается, как скопировать все фигуры с исходной страницы diagram.

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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
## **Скопируйте фигуру Visio в другой экземпляр фигуры.**
Метод копирования класса Shape использует экземпляр формы для клонирования.

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
## **Чтение данных формы Visio**
 Коллекция Props, предоставляемая классом Shape, поддерживает[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) объект. Свойство можно использовать для чтения данных фигуры (настраиваемые свойства).
### **Чтение всех свойств формы**
Чтобы определить пользовательские свойства в Microsoft Visio:

1. В diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Данные** , тогда**Данные формы** из меню.
 Все существующие свойства перечислены в диалоговом окне.

|**Данные фигуры, как показано в Microsoft Visio.**|** |
|:- |:- |
|![дело:изображение_альтернативный_текст](http://i.imgur.com/2loM7b0.png)||


|**Окно консоли, показывающее выходные данные формы.**|** |
|:- |:- |
|![дело:изображение_альтернативный_текст](http://i.imgur.com/kmAKNrx.png)||
#### **Читать пример программирования**
Фрагменты кода ниже считывают данные формы (настраиваемые свойства).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **Чтение свойства формы по имени**
Фрагмент кода ниже считывает свойство фигуры по имени (настраиваемое свойство).
#### **Пример программирования чтения по имени**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **Используйте индексы соединения для соединения фигур**
Aspose.Diagram for Java API уже позволяет разработчикам добавлять новые точки соединения на фигуру, и теперь разработчики могут соединять фигуры с помощью индексов соединения.
### **Используйте индексы соединения для соединения фигур**
Элемент connectShapesViaConnectorIndex, предоставляемый классом Page, можно использовать для соединения фигур с помощью индексов соединения. В следующем коде показано, как соединить фигуры:

1. Инициализировать новый рисунок.
1. Поместите четыре прямоугольника
1. Добавьте две дополнительные точки соединения, чтобы на нижней линии границы было три точки соединения.
1. Соедините первую фигуру от каждого нижнего соединения с тремя другими прямоугольными фигурами сверху с помощью динамических соединителей.
1. Сохранить рисунок
#### **Использование индексов соединения для соединения фигур Образец программирования**
Используйте следующий код в своем приложении Java для соединения фигур с помощью индексов соединения с Aspose.Diagram for Java API.

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
## **Получить родительскую форму подформы**
Aspose.Diagram for Java позволяет разработчикам извлекать родительскую форму подформы.
### **Получить родительскую форму**
Класс Shape предлагает свойство getParentShape для получения родительской формы.
#### **Получить пример программирования родительской фигуры**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
