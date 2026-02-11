---
title: Работа с гиперссылками
type: docs
weight: 160
url: /ru/net/working-with-hyperlinks/
description: В этом разделе объясняется, как добавить или получить гиперссылку в форме Visio с помощью Aspose.Diagram.
---
## **Добавить гиперссылку в форму Visio**
Microsoft Office Visio поддерживает добавление гиперссылок в любую фигуру. Гиперссылки могут указывать на другую страницу или фигуру в текущем чертеже, страницу или фигуру в другом чертеже, документ, отличный от чертежа Visio, веб-сайт, FTP-сайт или адрес электронной почты. Разработчики могут использовать Aspose.Diagram API, чтобы легко добавлять гиперссылки в фигуру Visio.

 В многостраничном чертеже Visio гиперссылки могут перемещать вас от одной формы к многим другим типам ссылок.[Коллекция гиперссылок](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) выставлены[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class предлагает метод Add, который можно использовать для добавления гиперссылки фигуры.

Чтобы идентифицировать свойства в Microsoft Office Visio:

1. В Visio diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Гиперссылка.**
1. Установить существующие свойства
1.  Нажимать**ХОРОШО** кнопка

**Данные гиперссылки фигуры, как показано в Microsoft Visio**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_1.png)
### **Добавить пример программирования гиперссылки**
Фрагмент кода ниже добавляет данные гиперссылки фигуры.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Получить данные гиперссылок для фигур Visio**
Разработчики могут получить все гиперссылки из формы Visio таким же образом, как они[читать данные формы Visio](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) с использованием[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

В многостраничном чертеже Visio гиперссылки могут перемещать вас от одной формы к многим другим типам ссылок.[Коллекция гиперссылок](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) выставлены[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class позволяет разработчикам извлекать гиперссылки.

Чтобы идентифицировать свойства в Microsoft Office Visio:

1. В diagram щелкните фигуру правой кнопкой мыши.
1.  Выбирать**Гиперссылка.**

Все существующие свойства перечислены в диалоговом окне.
**Данные гиперссылки фигуры, как показано в Microsoft Visio**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_1.png)

**Окно консоли, показывающее выходные данные формы**

![дело:изображение_альтернативный_текст](working-with-hyperlinks_3.png)
### **Получить пример программирования гиперссылок**
Фрагмент кода ниже считывает данные гиперссылки фигуры.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}
```
