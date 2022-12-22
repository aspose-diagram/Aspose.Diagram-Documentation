---
title: Работа со склеиванием фигур
type: docs
weight: 40
url: /ru/net/working-with-shapes-gluing/
description: В этом разделе объясняется, как получить фигуры, которые приклеиваются к определенной фигуре с помощью Aspose.Diagram.
---
## **Приклейте соединители к определенной форме**
[Добавить и соединить Visio фигуры](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for .NET. Также можно найти соединители, приклеенные к этой фигуре.
### **Получение склеенных фигур**
 Метод GluedShapes, предоставленный[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)можно использовать для получения списка идентификаторов всех соединителей, приклеенных к фигуре, или, если рассматриваемая фигура является соединителем, идентификаторы фигур, к которым он подключен.[Коллекция форм](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите список идентификаторов всех соединителей, приклеенных к этой фигуре.
#### **Пример программирования Get Connectors Glued**
Используйте следующий код в своем приложении .NET, чтобы найти все соединители, приклеенные к фигуре, используя Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Склейте Visio формы вместе с точкой соединения**
Aspose.Diagram for .NET позволяет разработчикам склеивать фигуры вместе через точки соединения.
### **Клеевые формы**
 Метод GlueShapes, предоставленный[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_1.png)</p>|<p>**diagram после склеивания фигур** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Клеевые фигуры.
1. Сохранить diagram.
#### **Glue Visio Образец программирования фигур**
Используйте следующий код в своем приложении .NET, чтобы склеить фигуры через точки соединения:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Приклейте фигуры внутри контейнера**
Aspose.Diagram for .NET позволяет разработчикам склеивать групповые фигуры внутри контейнера.
### **Форма группы клея**
 Метод GlueShapesInContainer, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_3.png)</p>|<p>**diagram после склеивания групповых форм** </p><p>![дело:изображение_альтернативный_текст](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Склеиваем фигурки групп.
1. Сохранить diagram.
#### **Склеивание фигур внутри примера программирования**
Используйте следующий код в своем приложении .NET, чтобы склеить фигуру группы внутри контейнера:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
