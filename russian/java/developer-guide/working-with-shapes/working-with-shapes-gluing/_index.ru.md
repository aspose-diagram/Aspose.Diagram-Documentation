---
title: Работа со склеиванием фигур
type: docs
weight: 10
url: /ru/java/working-with-shapes-gluing/
---
## **Приклейте соединители к определенной форме**
[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for Java. Также можно найти соединители, приклеенные к этой фигуре.
### **Получение склеенных фигур**
 Метод GluedShapes, предоставленный[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)можно использовать для получения списка идентификаторов всех соединителей, приклеенных к фигуре, или, если рассматриваемая фигура является соединителем, идентификаторы фигур, к которым он подключен.[Коллекция форм](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите список идентификаторов всех соединителей, приклеенных к этой фигуре.
#### **Пример программирования Get Connectors Glued**
Используйте следующий код в своем приложении Java, чтобы найти все соединители, приклеенные к фигуре, используя Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Склейте Visio формы вместе с точкой соединения**
Aspose.Diagram for Java позволяет разработчикам склеивать фигуры вместе через точки соединения.
### **Клеевые формы**
 Метод GlueShapes, предоставленный[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) можно использовать класс.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/Z69f4hg.png)</p>|<p>**diagram после склеивания фигур** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Клеевые фигуры.
1. Сохранить diagram.
#### **Glue Visio Образец программирования фигур**
Используйте следующий код в своем приложении Java, чтобы склеить фигуры через точки соединения:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Приклейте фигуры внутри контейнера**
Aspose.Diagram for Java позволяет разработчикам склеивать групповые фигуры внутри контейнера.
### **Форма группы клея**
Можно использовать метод GlueShapesInContainer, предоставляемый классом Page.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/HRRzIEh.png)</p>|<p>**diagram после склеивания групповых форм** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Склеиваем фигурки групп.
1. Сохранить diagram.
#### **Склеивание фигур внутри примера программирования**
Используйте следующий код в своем приложении Java, чтобы склеить фигуру группы внутри контейнера:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
