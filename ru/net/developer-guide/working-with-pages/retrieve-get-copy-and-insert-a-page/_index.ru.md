---
title: Получить, получить, скопировать и вставить страницу
type: docs
weight: 10
url: /ru/net/retrieve-get-copy-and-insert-a-page/
description: В этом разделе объясняется, как вставить страницу, скопировать страницу или получить информацию о странице с помощью Aspose.Diagram.
---
## **Получение информации о странице**
В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Чтобы получить информацию о странице, например идентификатор страницы и имя страницы, сначала определите, является ли страница фоновой или приоритетной.

[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page. Это свойство можно использовать для получения информации о странице.

Используйте свойство Page.Background, чтобы определить, является ли страница передним или фоновым.
### **Пример программирования получения информации о странице**
Следующий фрагмент кода извлекает информацию о страницах из файла diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-RetrievePageInfo-RetrievePageInfo.cs" >}}
## **Получите страницу Visio от Diagram**
Иногда разработчикам необходимо получить сведения о странице чертежа Visio. Aspose.Diagram имеет функции, которые помогают им в этом.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Page. Класс PageCollection предоставляет метод GetPage, который можно вызвать для получения объекта Page.
### **Получение объекта страницы Visio по идентификатору**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.

В следующем примере показано, как получить объект страницы по идентификатору из чертежа Visio.
#### **Пример программирования получения объекта страницы по идентификатору**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyID-GetVisioPagebyID.cs" >}}
### **Получение объекта страницы Visio по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.
#### **Пример программирования получения объекта страницы по имени**
В следующем примере показано, как получить объект страницы по имени из чертежа Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyName-GetVisioPagebyName.cs" >}}
## **Скопируйте страницу Visio в другую Diagram**
Aspose.Diagram for .NET API позволяет разработчикам копировать и добавлять свой контент из одного Visio diagram в другой. В этом разделе справки объясняется, как выполнить эту задачу.

 Aspose.Diagram for .NET API имеет[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Page. Класс PageCollection предоставляет метод Add, который можно вызывать для добавления другого объекта Page.

Этот пример работает следующим образом:

1. Создайте новый объект класса Diagram.
1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Добавить все мастера из загруженного Visio diagram
1. Получить объект страницы из загруженного diagram (который нужно скопировать).
1. Задайте имя и идентификатор объекта страницы.
1. Удалите пустую страницу нового diagram (необязательно).
1. Вызовите метод Add класса PageCollection.
1. Сохраните новый diagram в памяти компьютера.
### **Скопируйте пример программирования страницы Visio**
В приведенном ниже примере кода показано, как скопировать объект страницы Visio в другой чертеж Visio.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-CopyVisioPage-CopyVisioPage.cs" >}}
## **Скопируйте Visio страницу в другой экземпляр страницы**
Метод Copy класса Page берет экземпляр страницы для клонирования.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Вставка пустой страницы в чертеж Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) можно вставить новую пустую страницу в чертеж Microsoft Office Visio. В этом примере темы описано, как это сделать.

Метод Add, предоставляемый коллекцией Pages, позволяет разработчикам добавлять новую пустую страницу в Visio diagram. Необходимо назначить идентификатор страницы.
### **Вставьте образец программирования пустой страницы**
Следующий фрагмент кода вставляет пустую страницу в чертеж Visio:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.cs" >}}
## **Переместить позицию страницы на чертеже Visio**
Aspose.Diagram for .NET API может перемещать позицию страницы на чертеже Visio. Метод MoveTo, предоставляемый классом Page, помогает разработчикам перемещать позицию страницы.
### **Пример программирования перемещения страницы**
Элемент MoveTo принимает индекс целевой страницы в качестве параметра для перемещения позиции страницы на чертеже Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
