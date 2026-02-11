---
title: Получить, получить, скопировать и вставить страницу
type: docs
weight: 10
url: /ru/java/retrieve-get-copy-and-insert-a-page/
---
## **Получение информации о странице**
В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Чтобы получить информацию о странице, например идентификатор страницы и имя страницы, сначала определите, является ли страница фоновой или приоритетной.

[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](https://reference.aspose.com/diagram/java) Класс поддерживает набор объектов Aspose.Diagram.Page. Это свойство можно использовать для получения информации о странице.

Используйте свойство Page.Background, чтобы определить, является ли страница передним или фоновым.

На изображении ниже показан вывод фрагментов кода в этой статье.

**Консоль, показывающая вывод.** 

![дело:изображение_альтернативный_текст](retrieve-get-copy-and-insert-a-page_1.png)
### **Пример программирования получения информации о странице**
Следующий фрагмент кода извлекает информацию о страницах из файла diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}

## **Получите страницу Visio от Diagram**
Иногда разработчикам необходимо получить сведения о странице чертежа Visio. Aspose.Diagram имеет функции, которые помогают им в этом.

 Aspose.Diagram for Java предлагает[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Page. Класс PageCollection предоставляет метод GetPage, который можно вызвать для получения объекта Page.
### **Получение объекта страницы Visio по идентификатору**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.

В следующем примере показано, как получить объект страницы по идентификатору из чертежа Visio.
#### **Пример программирования получения объекта страницы по идентификатору**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}

### **Получение объекта страницы Visio по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.
#### **Пример программирования получения объекта страницы по имени**
В следующем примере показано, как получить объект страницы по имени из чертежа Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}

## **Скопируйте страницу Visio в другую Diagram**
Aspose.Diagram for Java API позволяет разработчикам копировать и добавлять свой контент из одного Visio diagram в другой. В этом разделе справки объясняется, как выполнить эту задачу.

 Aspose.Diagram for Java API имеет[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Page. Класс PageCollection предоставляет метод Add, который можно вызывать для добавления другого объекта Page.

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Скопируйте Visio страницу в другой экземпляр страницы**
Метод Copy класса Page берет экземпляр страницы для клонирования.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Вставка пустой страницы в чертеж Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) можно вставить новую пустую страницу в чертеж Microsoft Office Visio. В этом примере темы описано, как это сделать.

Метод Add, предоставляемый коллекцией Pages, позволяет разработчикам добавлять новую пустую страницу в Visio diagram. Необходимо назначить идентификатор страницы.
### **Вставьте образец программирования пустой страницы**
Следующий фрагмент кода вставляет пустую страницу в чертеж Visio:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Переместить позицию страницы на чертеже Visio**
Aspose.Diagram for Java API может перемещать позицию страницы на чертеже Visio. Метод moveTo, предоставляемый классом Page, помогает разработчикам перемещать позицию страницы.
### **Пример программирования перемещения страницы**
Элемент MoveTo принимает индекс целевой страницы в качестве параметра для перемещения позиции страницы на чертеже Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
