---
title: Работа с оконными элементами
type: docs
weight: 100
url: /ru/net/working-with-window-elements/
description: В этом разделе объясняется, как получить свойство оконных элементов в visio с Aspose.Diagram.
---
## **Извлечение оконных элементов из чертежа Visio**
 Главное окно приложения Visio может содержать любые открытые файлы Visio, точно так же, как современные веб-браузеры позволяют открывать несколько веб-страниц с вкладками в одном окне. Разработчики могут извлекать объекты Window, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) объект представляет собой список[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window)объекты, доступные на чертеже. Свойство Windows, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Window. Это свойство можно использовать для получения информации об окне, то есть идентификатора окна, типа, высоты, ширины и состояния.
### **Получить пример программирования оконных элементов**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}

## **Добавить элемент окна в Visio Diagram**
 Главное окно приложения Visio может содержать любые открытые файлы Visio, точно так же, как современные веб-браузеры позволяют открывать несколько веб-страниц с вкладками в одном окне. Теперь разработчики могут добавлять новый объект Window в экземпляр Microsoft Visio, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window) объект представляет открытое окно в экземпляре Microsoft Visio.[Добавлять](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) метод, раскрытый[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, позволяет добавить новый объект Window.
### **Добавить пример программирования элемента окна**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Добавить поддержку динамических сеток и точек подключения**
Динамическая сетка помогает размещать новые фигуры по вертикали и горизонтали относительно фигур, которые вы уже разместили на чертеже. Что касается точек подключения, после того, как они отмечены как отмеченные, это поможет нам увидеть точки подключения, когда мы находимся в процессе подключения к ним. Мы можем достичь обоих вариантов, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Поддержка динамических сеток и точек соединения в чертежах Visio**
[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class предлагает свойства DynamicGridEnabled и ShowConnectionPoints. Эти свойства можно использовать для применения настроек для поддержки динамических сеток и отображения параметров точек соединения.
#### **Добавить пример программы поддержки**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram**
 Microsoft Office Visio имеет пару линеек, сетку и два типа направляющих и флаг разрыва страницы, чтобы увидеть, что будет напечатано на каждой странице. Разработчики могут применить эти настройки, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Настройки применяются глобально к одной странице.

[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window)class предлагает свойства ShowGrid, ShowGuides, ShowRulers и ShowPageBreaks. Эти свойства можно использовать для применения настроек для отображения и скрытия сеток, направляющих, линеек и разрывов страниц.
### **Образец программирования**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

