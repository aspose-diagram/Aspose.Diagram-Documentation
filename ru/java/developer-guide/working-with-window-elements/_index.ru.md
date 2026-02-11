---
title: Работа с оконными элементами
type: docs
weight: 130
url: /ru/java/working-with-window-elements/
---
## **Извлечение оконных элементов из чертежа Visio**
 Главное окно приложения Visio может содержать любые открытые файлы Visio, точно так же, как современные веб-браузеры позволяют открывать несколько веб-страниц с вкладками в одном окне. Разработчики могут извлекать объекты Window, используя[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

[WindowCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection) объект представляет собой список[Окно](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)объекты, доступные на чертеже. Свойство Windows, предоставляемое классом Diagram, поддерживает коллекцию объектов Aspose.Diagram.Window. Это свойство можно использовать для получения информации об окне, то есть идентификатора окна, типа, высоты, ширины и состояния.

**Окно консоли, показывающее вывод кода.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/zduARGh.png)
### **Получить пример программирования оконных элементов**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}

## **Добавить элемент окна в Visio Diagram**
 Главное окно приложения Visio может содержать любые открытые файлы Visio, точно так же, как современные веб-браузеры позволяют открывать несколько веб-страниц с вкладками в одном окне. Теперь разработчики могут добавлять новый объект Window в экземпляр Microsoft Visio, используя[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

Объект Window представляет открытое окно в экземпляре Microsoft Visio. Метод Add, предоставляемый классом WindowCollection, позволяет добавить новый объект Window.
### **Добавить пример программирования элемента окна**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Добавить поддержку динамических сеток и точек подключения**
Динамическая сетка помогает размещать новые фигуры по вертикали и горизонтали относительно фигур, которые вы уже разместили на чертеже. Что касается точек подключения, после того, как они отмечены как отмеченные, это поможет нам увидеть точки подключения, когда мы находимся в процессе подключения к ним. Мы можем достичь обоих вариантов, используя[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Поддержка динамических сеток и точек соединения в чертежах Visio**
Класс Window предлагает свойства DynamicGridEnabled и ShowConnectionPoints. Эти свойства можно использовать для применения настроек для поддержки динамических сеток и отображения параметров точек соединения.

**Приложение Visio, показывающее параметры в Visio.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/bxsJIwF.png)
#### **Добавить пример программы поддержки**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram**
 Microsoft Office Visio имеет пару линеек, сетку и два типа направляющих и флаг разрыва страницы, чтобы увидеть, что будет напечатано на каждой странице. Разработчики могут применить эти настройки, используя[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)Настройки применяются глобально к одной странице.

Класс Window предлагает свойства ShowGrid, ShowGuides, ShowRulers и ShowPageBreaks. Эти свойства можно использовать для применения настроек для отображения и скрытия сеток, направляющих, линеек и разрывов страниц.

**Приложение Visio, показывающее параметры в Visio.**

![дело:изображение_альтернативный_текст](http://i.imgur.com/E0pvXbP.png)
### **Образец программирования**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

