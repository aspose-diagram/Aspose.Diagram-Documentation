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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-RetrieveWindowElementsOfDiagram-RetrieveWindowElementsOfDiagram.cs" >}}
## **Добавить элемент окна в Visio Diagram**
 Главное окно приложения Visio может содержать любые открытые файлы Visio, точно так же, как современные веб-браузеры позволяют открывать несколько веб-страниц с вкладками в одном окне. Теперь разработчики могут добавлять новый объект Window в экземпляр Microsoft Visio, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window) объект представляет открытое окно в экземпляре Microsoft Visio.[Добавлять](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) метод, раскрытый[WindowCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class, позволяет добавить новый объект Window.
### **Добавить пример программирования элемента окна**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-AddWindowElementInVisio-AddWindowElementInVisio.cs" >}}
## **Добавить поддержку динамических сеток и точек подключения**
Динамическая сетка помогает размещать новые фигуры по вертикали и горизонтали относительно фигур, которые вы уже разместили на чертеже. Что касается точек подключения, после того, как они отмечены как отмеченные, это поможет нам увидеть точки подключения, когда мы находимся в процессе подключения к ним. Мы можем достичь обоих вариантов, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Поддержка динамических сеток и точек соединения в чертежах Visio**
[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window) class предлагает свойства DynamicGridEnabled и ShowConnectionPoints. Эти свойства можно использовать для применения настроек для поддержки динамических сеток и отображения параметров точек соединения.
#### **Добавить пример программы поддержки**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-AddSupportOfVisualAids-AddSupportOfVisualAids.cs" >}}
## **Показать и скрыть сетки, линейки, направляющие и разрывы страниц Visio Diagram**
 Microsoft Office Visio имеет пару линеек, сетку и два типа направляющих и флаг разрыва страницы, чтобы увидеть, что будет напечатано на каждой странице. Разработчики могут применить эти настройки, используя[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)Настройки применяются глобально к одной странице.

[Окно](http://www.aspose.com/api/net/diagram/aspose.diagram/window)class предлагает свойства ShowGrid, ShowGuides, ShowRulers и ShowPageBreaks. Эти свойства можно использовать для применения настроек для отображения и скрытия сеток, направляющих, линеек и разрывов страниц.
### **Образец программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Window-Elements-DisplayGridsRulersGuidesAndPageBreaks-DisplayGridsRulersGuidesAndPageBreaks.cs" >}}
