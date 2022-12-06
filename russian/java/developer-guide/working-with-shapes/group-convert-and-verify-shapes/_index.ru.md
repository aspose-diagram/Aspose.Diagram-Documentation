---
title: Группируйте, конвертируйте и проверяйте фигуры
type: docs
weight: 50
url: /ru/java/group-convert-and-verify-shapes/
---
## **Сгруппируйте несколько фигур вместе на чертеже Visio**
Aspose.Diagram API позволяет разработчикам группировать фигуры вместе, чтобы перемещать их все одновременно. Каждая фигура в группе имеет уникальный идентификатор и собственный набор свойств. Когда мы изменяем форматирование группы фигур, оно присваивает новое свойство каждой фигуре.
### **Как сгруппировать фигуры**
Метод Group, предоставляемый классом ShapeCollection, можно использовать для группировки фигур.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. инициализировал массив фигур
1. получить определенную форму по идентификатору.
1. получить другую конкретную форму по идентификатору.
1. назначать фигуры массиву.
1. сгруппируйте фигуры, вызвав метод Group.
1. сохранить diagram
#### **Образец программирования групповых форм**
Используйте следующий код в приложении Java для группировки фигур с помощью Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Преобразование формы Visio в другие форматы файлов**
Aspose.Diagram for Java API позволяет разработчикам преобразовывать одну форму Visio в любой другой поддерживаемый формат файла. В этой статье мы удалим все остальные фигуры Visio со страницы и настроим параметры страницы в соответствии с исходным размером фигуры.
### **Преобразование определенной формы Visio**
 Разработчики могут преобразовать форму Visio в PDF, HTML, изображение, SVG и SWF с помощью[указав параметры сохранения Visio]().
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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Конвертировать форму Visio в PDF**
Метод ToPdf класса Shape позволяет преобразовать фигуру в формат PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Конвертировать форму Visio в HTML**
Метод ToHTML класса Shape позволяет преобразовать фигуру в формат HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}} 
## **Проверьте, соединены или склеены две фигуры Visio**
 Aspose.Diagram for Java API позволяет разработчикам проверить, что две фигуры Visio склеены или соединены. Ранее мы видели, как мы можем соединить или склеить две фигуры в этих разделах справки:[Добавить и соединить Visio фигуры](/diagram/ru/java/add-and-connect-visio-shapes/) а также[Приклейте фигуры внутри контейнера](/diagram/ru/java/working-with-shapes-gluing/).
### **Проверка соединенных или склеенных фигур**
[Форма](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class предлагает свойства IsGlued и IsConnected, чтобы определить, склеены ли две фигуры или соединены.
#### **Пример программирования проверки соединенных или склеенных фигур**
Следующий фрагмент кода проверяет, соединены ли две фигуры или склеены.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Проверьте, входит ли фигура Visio в группу фигур**
Aspose.Diagram for Java API позволяет разработчикам проверять, входит ли фигура Visio в группу фигур или нет.
### **Проверка формы в группе фигур**
Класс Shape предлагает свойства IsInGroup, чтобы определить, является ли фигура Visio фигурой группы.
#### **Проверка формы в примере программирования группы фигур**
Следующий фрагмент кода проверяет, является ли фигура групповой.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 Будем рады вашим вопросам и предложениям на[Aspose.Diagram Форум](https://forum.aspose.com/c/diagram/17). Мы ответим быстро.

{{% /alert %}}
