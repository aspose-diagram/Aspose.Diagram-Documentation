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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Получите страницу Visio от Diagram**
Иногда разработчикам необходимо получить сведения о странице чертежа Visio. Aspose.Diagram имеет функции, которые помогают им в этом.

 Aspose.Diagram for .NET предлагает[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Page. Класс PageCollection предоставляет метод GetPage, который можно вызвать для получения объекта Page.
### **Получение объекта страницы Visio по идентификатору**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.

В следующем примере показано, как получить объект страницы по идентификатору из чертежа Visio.
#### **Пример программирования получения объекта страницы по идентификатору**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Получение объекта страницы Visio по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.
#### **Пример программирования получения объекта страницы по имени**
В следующем примере показано, как получить объект страницы по имени из чертежа Visio.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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
