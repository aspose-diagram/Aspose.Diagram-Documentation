---
title: Вращение, изменение положения и соединение подформ
type: docs
weight: 30
url: /ru/net/rotate-change-the-position-and-connect-sub-shapes/
description: В этом разделе объясняется, как повернуть фигуру visio с помощью Aspose.Diagram.
---
## **Повернуть фигуру на подходящий угол**
 Aspose.Diagram for .NET позволяет поворачивать фигуру под любым углом. Метод SetAngle, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) можно использовать для поворота фигуры на любой желаемый угол. Он принимает один параметр в качестве угла.
### **Поворот образца программирования формы**
Используйте следующий код в своем приложении .NET, чтобы повернуть фигуру с помощью Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-RotateVisioShape-RotateVisioShape.cs" >}}
## **Изменить положение фигуры**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Класс позволяет изменить положение фигуры. Соединительная линия автоматически настраивается, когда фигура перемещается в другое положение. Методы Move и MoveTo, предоставляемые[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, поддерживают изменение положения фигуры как части группы или нет. Примеры кода в этой статье перемещают фигуру на странице.

Процесс перемещения фигуры:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Переместить фигуру в другое место
1. Сохраните номер diagram.
### **Пример программирования изменения позиции**
Фрагмент кода ниже показывает, как переместить фигуру. Код извлекает страницу Visio по имени и форме по идентификатору 16 и перемещает ее позицию.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-MoveVisioShape-MoveVisioShape.cs" >}}
## **Соедините подформы групп**
 В этом разделе подробно описывается, как соединить два подфигуры двух разных групповых фигур на диаграммах Microsoft Visio с помощью Aspose.Diagram for .NET. Метод ConnectShapesViaConnector, предоставляемый[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) можно использовать для соединения фигур по их идентификаторам. Метод AddShape, представленный[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)class, можно использовать для добавления формы.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной странице.
1. Добавьте форму динамического соединителя на выбранную страницу.
1. Подключить подформы
### **Образец программирования Connect Sub-Shapes**
Используйте следующий код в своем приложении .NET, чтобы соединить подформы двух разных фигур группы, используя Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.cs" >}}
## **Соедините фигуры с определенной фигурой**
[Добавить и соединить Visio фигуры](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) объясняет, как добавить фигуру и соединить ее с другими фигурами на диаграммах Microsoft Visio, используя Aspose.Diagram for .NET. Также можно найти фигуры, которые связаны с определенной фигурой.

 Метод ConnectedShapes, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) можно использовать для получения идентификаторов фигур, связанных с фигурой. Метод GetShape, представленный[Коллекция форм](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) class, затем можно использовать для поиска фигуры по ее идентификатору.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. Доступ к определенной форме.
1. Получите имена всех фигур, связанных с выбранной фигурой.
### **Получить пример программирования фигур**
Используйте следующий код в своем приложении .NET, чтобы найти все фигуры, связанные с определенной фигурой, используя Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.cs" >}}
