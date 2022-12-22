---
title: Вращение, изменение положения и соединение подформ
type: docs
weight: 60
url: /ru/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Повернуть фигуру на подходящий угол**
 Aspose.Diagram for Java позволяет поворачивать фигуру под любым углом. Метод SetAngle, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) можно использовать для поворота фигуры на любой желаемый угол. Он принимает один параметр в качестве угла.
### **Поворот образца программирования формы**
Используйте следующий код в своем приложении Java, чтобы повернуть фигуру с помощью Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Изменить положение фигуры**
Класс Shape позволяет изменить положение фигуры. Соединительная линия автоматически настраивается, когда фигура перемещается в другое положение.

Методы Move и MoveTo, предоставляемые классом Shape, поддерживают изменение положения фигуры как части группы или нет.
Примеры кода в этой статье перемещают фигуру на странице.
**Ввод diagram** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/cThgWnB.png)


**diagram после перемещения формы** 

![дело:изображение_альтернативный_текст](http://i.imgur.com/Q3QByqe.png)

Процесс перемещения фигуры:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Переместить фигуру в другое место
1. Сохраните номер diagram.
### **Пример программирования изменения позиции**
Фрагмент кода ниже показывает, как переместить фигуру. Код извлекает страницу Visio по имени и форме по идентификатору 16 и перемещает ее позицию.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Соедините подформы групп**
В этом разделе подробно описывается, как соединить два подфигуры двух разных форм групп на диаграммах Microsoft Visio с использованием Aspose.Diagram for Java.

 Метод ConnectShapesViaConnector, предоставляемый[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) можно использовать для соединения фигур по их идентификаторам. Метод AddShape, представленный[Diagram](https://reference.aspose.com/diagram/java)class, можно использовать для добавления формы.

|<p>**Ввод diagram** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/74rDby5.png)</p>|<p>**diagram после соединения подформ** </p><p>![дело:изображение_альтернативный_текст](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной странице.
1. Добавьте форму динамического соединителя на выбранную страницу.
1. Подключить подформы
### **Образец программирования Connect Sub-Shapes**
Используйте следующий код в своем приложении Java, чтобы соединить подформы двух разных фигур группы, используя Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Соедините фигуры с определенной фигурой**
[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for Java. Также можно найти фигуры, которые связаны с определенной фигурой.

 Метод ConnectedShapes, предоставляемый[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) можно использовать для получения идентификаторов фигур, связанных с фигурой. Метод GetShape, представленный[Коллекция форм](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите имена всех фигур, связанных с выбранной фигурой.
### **Получить пример программирования фигур**
Используйте следующий код в своем приложении Java, чтобы найти все фигуры, связанные с определенной фигурой, используя Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
