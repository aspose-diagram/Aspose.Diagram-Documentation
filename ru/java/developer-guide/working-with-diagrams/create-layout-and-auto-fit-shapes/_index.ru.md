---
title: Создание, компоновка и автоматическая подгонка фигур
type: docs
weight: 10
url: /ru/java/create-layout-and-auto-fit-shapes/
---
## **Создание Diagram**
 Aspose.Diagram for Java позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](/diagram/ru/java/add-and-connect-visio-shapes/)для создания diagram. Используйте конструктор по умолчанию[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-CreateDiagram-CreateDiagram.java" >}}
## **Формы макета в стиле блок-схемы**
 С определенными типами подключенных чертежей, такими как блок-схемы и сетевые диаграммы, вы можете использовать**Формы макета** функция автоматического позиционирования фигур. Автоматическое позиционирование выполняется быстрее, чем ручное перетаскивание каждой фигуры в новое место.

Например, если вы обновляете большую блок-схему, чтобы включить новый процесс, вы можете добавить и соединить фигуры, составляющие процесс, а затем использовать функцию макета для автоматического макета обновленного рисунка.

 Метод Layout, представленный[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class размещает фигуры и/или перенаправляет соединители на всех страницах diagram. Этот метод принимает объект LayoutOptions в качестве аргумента. Используйте различные свойства, предоставляемые классом LayoutOptions, для автоматического размещения фигур.

На изображении ниже показан код diagram, загруженный фрагментами кода в этой статье, до применения автоматического макета. Фрагменты кода показывают, как подать заявку[макеты блок-схем](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/) а также[компактные макеты дерева](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/).

**Источник diagram.** 

![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_1.png)

Фрагменты кода в этой статье берут исходный код diagram и применяют к нему несколько типов автоматической разметки, сохраняя каждый в отдельном файле.

|<p>**Формы макета снизу вверх** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Формы макета сверху вниз** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Формы макета слева направо** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Формы макета справа налево** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_5.png)</p>|
Чтобы разместить фигуры в стиле блок-схемы:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр класса LayoutOptions и задайте свойства, связанные со стилем блок-схемы.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать рисунок Visio.
### **Пример программирования в стиле блок-схемы**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.java" >}}
### **Размещение фигур в стиле компактного дерева**
 Компактный стиль компоновки дерева пытается построить древовидную структуру. Он использует тот же входной файл, что и[пример выше](/diagram/ru/java/create-2c-layout-and-auto-fit-shapes/)и сохраняет в несколько различных стилей компактного дерева.

|<p>**Компактное древовидное расположение — вниз и вправо** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Компактное древовидное расположение — вниз и влево** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Компактная древовидная компоновка - справа и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Компактное древовидное расположение — слева и снизу** </p><p>![дело:изображение_альтернативный_текст](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Чтобы разместить фигуры в компактном древовидном стиле:

1.  Создайте экземпляр[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) учебный класс.
1. Создайте экземпляр класса LayoutOptions и задайте свойства стиля компактного дерева.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать файл Visio.
#### **Пример программирования в стиле компактного дерева**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.java" >}}
## **Автоматическая установка Visio Diagram**
Aspose.Diagram API поддерживает автоматическую подгонку чертежа Visio. Эта функция помогает помещать внешние фигуры внутрь границ страницы Visio.

Aspose.Diagram for Java API имеет класс Diagram, представляющий чертеж Visio. Класс DiagramSaveOptions предоставляет свойство AutoFitPageToDrawingContent для автоматического подбора чертежа Visio.

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Создайте объект класса DiagramSaveOptions и передайте результирующий формат файла.
1. Установите свойство AutoFitPageToDrawingContent объекта DiagramSaveOptions.
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования автоматической подгонки**
В следующем примере кода показано, как автоматически подгонять фигуры в Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.java" >}}
## **Работа с проектом VBA**
### **Изменить код модуля VBA в Visio Diagram**
В этой статье показано, как автоматически изменить код модуля VBA с помощью Aspose.Diagram for Java.

Мы добавили классы VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference и VbaProjectReferenceCollection. Эти классы помогают получить контроль над проектом VBA. Разработчики могут извлекать и изменять код модуля VBA.
### **Изменить пример программирования кода модуля VBA**
Пожалуйста, проверьте этот пример кода:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-ModifyVBAModuleCode-ModifyVBAModuleCode.java" >}}
### **Удалить все макросы из Visio Diagram**
Aspose.Diagram for Java позволяет разработчикам удалить все макросы из файла Visio diagram.

Свойство JavaProjectData, предоставляемое[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, позволяет удалить все макросы из чертежа Visio.
### **Пример программирования удаления всех макросов**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.java" >}}
