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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GroupShapes-GroupShapes.cs" >}}
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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.cs" >}}
## **Проверьте, входит ли фигура Visio в группу фигур**
Aspose.Diagram for .NET API позволяет разработчикам проверять, входит ли фигура Visio в группу фигур или нет.
### **Проверка формы в группе фигур**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class предлагает свойства IsInGroup, чтобы определить, является ли фигура Visio фигурой группы.
#### **Проверка формы в примере программирования группы фигур**
Следующий фрагмент кода проверяет, является ли фигура групповой.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.cs" >}}
