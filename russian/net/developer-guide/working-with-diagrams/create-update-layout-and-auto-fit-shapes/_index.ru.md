---
title: Создание, обновление, компоновка и автоматическая подгонка фигур
type: docs
weight: 10
url: /ru/net/create-update-layout-and-auto-fit-shapes/
description: Используйте C# Diagram API для создания, обновления и автоматического размещения фигур в файлах Visio с помощью C# в ваших приложениях. Полное руководство с примерами кода C#.
---
## **Создание Diagram**
 Aspose.Diagram for .NET позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)для создания diagram. Используйте конструктор по умолчанию[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Формы макета в стиле блок-схемы**
 С определенными типами подключенных чертежей, такими как блок-схемы и сетевые диаграммы, вы можете использовать**Формы макета** функция автоматического позиционирования фигур. Автоматическое позиционирование выполняется быстрее, чем ручное перетаскивание каждой фигуры в новое место.

Например, если вы обновляете большую блок-схему, чтобы включить новый процесс, вы можете добавить и соединить фигуры, составляющие процесс, а затем использовать функцию макета для автоматического макета обновленного рисунка.

 Метод Layout, представленный[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class размещает фигуры и/или перенаправляет соединители на всех страницах diagram. Этот метод принимает[МакетОпции](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)объект в качестве аргумента. Используйте различные свойства, предоставляемые классом LayoutOptions, для автоматического размещения фигур.

На изображении ниже показан код diagram, загруженный фрагментами кода в этой статье, до применения автоматического макета. Фрагменты кода показывают, как подать заявку[макеты блок-схем](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) а также[компактные макеты дерева](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**Источник diagram.**

![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_1.png)

Фрагменты кода в этой статье берут исходный код diagram и применяют к нему несколько типов автоматической разметки, сохраняя каждый в отдельном файле.

|<p>**Формы макета снизу вверх** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Формы макета сверху вниз** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Формы макета слева направо** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Формы макета справа налево** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Чтобы разместить фигуры в стиле блок-схемы:

1. Создайте экземпляр класса Diagram.
1. Создайте экземпляр класса LayoutOptions и задайте свойства, связанные со стилем блок-схемы.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать рисунок Visio.
### **Пример программирования в стиле блок-схемы**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Размещение фигур в стиле компактного дерева**
 Компактный стиль компоновки дерева пытается построить древовидную структуру. Он использует тот же входной файл, что и[пример выше](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)и сохраняет в несколько различных стилей компактного дерева.

|<p>**Компактное древовидное расположение — вниз и вправо** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Компактное древовидное расположение — вниз и влево** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Компактная древовидная компоновка - справа и снизу** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Компактное древовидное расположение — слева и снизу** </p><p>![дело:изображение_альтернативный_текст](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Чтобы разместить фигуры в компактном древовидном стиле:

1.  Создайте экземпляр[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) учебный класс.
1. Создайте экземпляр класса LayoutOptions и задайте свойства стиля компактного дерева.
1. Вызовите метод Layout класса Diagram, передав LayoutOptions.
1. Вызовите метод Save класса Diagram, чтобы записать файл Visio.
#### **Пример программирования в стиле компактного дерева**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Автоматическая установка Visio Diagram**
 Aspose.Diagram API поддерживает автоматическую подгонку чертежа Visio. Эта функция помогает помещать внешние фигуры внутрь границ страницы Visio. Aspose.Diagram for .NET API имеет[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio.[ДиаграммаСохранитьОпции](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) Класс предоставляет свойство AutoFitPageToDrawingContent для автоматического подбора размера чертежа Visio.

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Создайте объект класса DiagramSaveOptions и передайте результирующий формат файла.
1. Установите свойство AutoFitPageToDrawingContent объекта DiagramSaveOptions.
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования автоматической подгонки**
В следующем примере кода показано, как автоматически подгонять фигуры в Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **Работа с проектом VBA**
### **Изменить код модуля VBA в Visio Diagram**
 В этой статье показано, как автоматически изменить код модуля VBA с помощью Aspose.Diagram for .NET. Мы добавили[VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [ВбаМодулеКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) а также[ВбаПрожектРеференсКоллекшн](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) классы. Эти классы помогают получить контроль над проектом VBA. Разработчики могут извлекать и изменять код модуля VBA.
### **Изменить пример программирования кода модуля VBA**
Пожалуйста, проверьте этот пример кода:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Удалить все макросы из Visio Diagram**
 Aspose.Diagram for .NET позволяет разработчикам удалять все макросы из Visio diagram. Свойство VbProjectData, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, позволяет удалить все макросы из чертежа Visio.
### **Пример программирования удаления всех макросов**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **Создание нового Diagram с помощью VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)позволяет разработчикам создавать и работать с Microsoft Office Visio диаграммами и включать функции в свои программные приложения. Есть и другие способы работы с файлами Visio, чаще всего Microsoft Автоматизация. К сожалению, это имеет некоторые ограничения. Aspose.Diagram является мощным и быстрым и работает независимо без установки Microsoft Office.

 В этой статье о миграции показано, как сначала использовать[ВСТО](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) а потом[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) чтобы создать новый diagram и добавить к нему несколько фигур. Вы заметите, что код Aspose.Diagram короче кода VSTO. Не стесняйтесь использовать код в качестве основы для собственной разработки и улучшать его в соответствии с вашими потребностями. VSTO позволяет программировать Microsoft Visio файлов. Чтобы создать новый diagram:

1. Создайте объект приложения Visio.
1. Сделать объект приложения невидимым.
1. Создайте пустой diagram.
1. Добавьте формы из мастеров Visio (трафареты).
1. Сохраните файл как VDX.
### **Создайте новый Diagram с образцом программирования VSTO**
{{% alert color="primary" %}}

используя Visio = Microsoft.Office.Interop.Visio;
Импорт Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Пример:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Создание нового Diagram с Aspose.Diagram for .NET**
При использовании Aspose.Diagram API разработчикам не требуется установка Microsoft Office Visio на машину, и они могут работать независимо от Microsoft Office Автоматизация.

Чтобы создать новый diagram:

1. Создайте пустой diagram.
1. Добавьте формы из мастеров Visio (трафареты).
1. Сохраните файл как VDX.
### **Новый Diagram с образцом программирования Aspose.Diagram for .NET**
{{% alert color="primary" %}}

используя Aspose.Diagram;
Импорт Aspose.Diagram

{{% /alert %}}

Пример:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Обновить свойства фигуры**
 При работе с диаграммами Microsoft Visio пользователи могут обновлять атрибуты фигуры, включая текст, стиль, положение, высоту и ширину. Как разработчик программного обеспечения, работающий с файлами Visio, вам будет предложено сделать это программно. Хорошая новость заключается в том, что это возможно либо с использованием механизмов программирования с файлами Visio, которые предоставляет Microsoft, VSTO, либо с использованием[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Ниже в теме показано, как использовать[ВСТО](https://products.aspose.com/diagram/net/) а также[Aspose.Diagram](https://products.aspose.com/diagram/net/) для обновления свойств фигуры. Фрагменты кода ниже показывают, как обновить свойства формы для VSTO и Aspose.Diagram for .NET. Не стесняйтесь использовать код и применять его в своей конкретной ситуации.
### **Обновление свойств формы с помощью VSTO**
VSTO позволяет программировать Microsoft Visio файлов. Чтобы обновить свойства фигуры:

1. Создайте объект приложения Visio.
1. Сделать объект приложения невидимым.
1. Откройте существующий файл Visio VSD.
1. Найдите нужную форму.
1. Обновите свойства фигуры (текст, стиль текста, положение и размер).
1. Сохраните файл как VDX.
#### **Обновление свойств формы с помощью примера программирования VSTO**
{{% alert color="primary" %}}

используя Visio = Microsoft.Office.Interop.Visio;
Импорт Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Пример:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Обновление свойств формы с помощью Aspose.Diagram for .NET**
Используя Aspose.Diagram API, разработчикам не нужно Microsoft Office Visio на машине, и они могут работать независимо от Microsoft Office Автоматизация.

Чтобы обновить свойства фигуры с помощью Aspose.Diagram for .NET:

1. Откройте существующий файл Visio VSD.
1. Найдите нужную форму.
1. Обновите свойства фигуры (текст, стиль текста, положение и размер).
1. Сохраните файл как VDX.
#### **Обновление свойств формы с помощью примера программы Aspose.Diagram for .NET**
{{% alert color="primary" %}}

используя Aspose.Diagram;
Импорт Aspose.Diagram

{{% /alert %}}

**Пример:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
