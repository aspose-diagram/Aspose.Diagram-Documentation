---
title: Группируйте, конвертируйте и проверяйте фигуры
type: docs
weight: 80
url: /ru/net/group-convert-and-verify-shapes/
description: В этом разделе объясняется, как группировать фигуры с помощью Aspose.Diagram.
---
## **Сгруппируйте несколько фигур вместе на чертеже Visio**
Aspose.Diagram API позволяет разработчикам группировать фигуры вместе, чтобы перемещать их все одновременно. Каждая фигура в группе имеет уникальный идентификатор и собственный набор свойств. Когда мы изменяем форматирование группы фигур, оно присваивает новое свойство каждой фигуре.
### **Как сгруппировать фигуры**
 Метод Group, представленный[Коллекция форм](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) класс можно использовать для группировки фигур вместе.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. инициализировал массив фигур
1. получить определенную форму по идентификатору.
1. получить другую конкретную форму по идентификатору.
1. назначать фигуры массиву.
1. сгруппируйте фигуры, вызвав метод Group.
1. сохранить diagram
#### **Образец программирования групповых форм**
Используйте следующий код в приложении .NET для группировки фигур с помощью Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Преобразование формы Visio в другие форматы файлов**
Aspose.Diagram for .NET API позволяет разработчикам преобразовывать одну форму Visio в любой другой поддерживаемый формат файла. В этой статье мы удалим все остальные фигуры Visio со страницы и настроим параметры страницы в соответствии с исходным размером фигуры.
### **Преобразование определенной формы Visio**
 Разработчики могут преобразовать форму Visio в PDF, HTML, изображение, SVG и SWF с помощью**указав параметры сохранения Visio**.
Этот пример кода работает следующим образом:

1. Загрузите источник Visio.
1. Получить конкретную страницу.
1. Удалите фоновую страницу.
1. Создайте хеш-таблицу всех форм, содержащих идентификаторы и имена.
1. Итерация по хеш-таблице
1. Удалите все фигуры со страницы Visio, кроме одной.
1. Установите размер страницы.
1. Сохраните страницу Visio в любом поддерживаемом формате файла.
#### **Образец программирования преобразования формы**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}
```
### **Преобразование формы Visio в форму PDF**
Метод ToPdf класса Shape позволяет преобразовать фигуру в формат PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Преобразование формы Visio в форму HTML**
Метод ToHTML класса Shape позволяет преобразовать фигуру в формат HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Проверьте, соединены или склеены две фигуры Visio**
 Aspose.Diagram for .NET API позволяет разработчикам проверить, что две фигуры Visio склеены или соединены. Ранее мы видели, как мы можем соединить или склеить две фигуры в этих разделах справки:[Добавить и соединить Visio фигуры](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) а также[Приклейте фигуры внутри контейнера](/diagram/ru/net/working-with-shapes-gluing/).
### **Проверка соединенных или склеенных фигур**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class предлагает свойства IsGlued и IsConnected, чтобы определить, склеены ли две фигуры или соединены.
#### **Пример программирования проверки соединенных или склеенных фигур**
Следующий фрагмент кода проверяет, соединены ли две фигуры или склеены.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}
```
## **Проверьте, входит ли фигура Visio в группу фигур**
Aspose.Diagram for .NET API позволяет разработчикам проверять, входит ли фигура Visio в группу фигур или нет.
### **Проверка формы в группе фигур**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class предлагает свойства IsInGroup, чтобы определить, является ли фигура Visio фигурой группы.
#### **Проверка формы в примере программирования группы фигур**
Следующий фрагмент кода проверяет, является ли фигура групповой.

```
{{< highlight "csharp" >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}
```
