---
title: Работа с гиперссылками
type: docs
weight: 110
url: /ru/java/working-with-hyperlinks/
---
## **Добавить гиперссылку в форму Visio**
Это простой способ динамически добавить гиперссылку в форму Microsoft Visio.

На многостраничных Visio чертежах гиперссылки могут перемещать вас с одной страницы на другую. Вы также можете связать свой рисунок с веб-страницей или файлом в вашей системе.

Эти свойства выявляются[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) класс поддерживает[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) объект. Метод add можно использовать для добавления данных гиперссылки фигуры.

Чтобы идентифицировать свойства в Microsoft Visio:

1. В diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Гиперссылка**.
1. Установить существующие свойства
1.  Нажимать**ХОРОШО** кнопка

**Данные гиперссылки фигуры, как показано в Microsoft Visio**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_1.png)

Фрагменты кода ниже добавляют данные гиперссылки фигуры.
### **Добавить пример программирования гиперссылки**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Получить данные гиперссылок для фигур Visio**
 Данные гиперссылки фигуры можно получить тем же способом, что и[чтение данных формы Visio]().

Разработчики могут получить все гиперссылки из формы Visio таким же образом, как они[читать данные формы Visio]() с использованием[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

В многостраничных Visio чертежах гиперссылки могут перемещать вас с одной страницы на другую. Вы также можете связать свой рисунок с веб-страницей или файлом в вашей системе.

Эти свойства выявляются[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) класс поддерживает[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)объект. Свойство можно использовать для чтения данных гиперссылки фигуры.

Чтобы идентифицировать свойства в Microsoft Visio:

1. В diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Гиперссылка.**
 Все существующие свойства перечислены в диалоговом окне.

**Данные гиперссылки фигуры, как показано в Microsoft Visio**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_2.png)

**Окно консоли, показывающее выходные данные формы**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_3.png)

Фрагменты кода ниже считывают данные гиперссылки фигуры.
### **Получить пример программирования гиперссылок**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}
```
