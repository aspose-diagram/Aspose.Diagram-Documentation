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
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```
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
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
string fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.LayoutStyle = LayoutStyle.FlowChart;
flowChartOptions.SpaceShapes = 1f;
flowChartOptions.EnlargePage = true;

// Set layout direction as BottomToTop and then save
flowChartOptions.Direction = LayoutDirection.BottomToTop;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_btm_top_out.vdx", SaveFileFormat.VDX);

// Set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.TopToBottom;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_top_btm_out.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.LeftToRight;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_left_right_out.vdx", SaveFileFormat.VDX);

// Set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.Direction = LayoutDirection.RightToLeft;
diagram.Layout(flowChartOptions);
diagram.Save(dataDir + "sample_right_left_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
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
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

string fileName = "LayOutShapesInCompactTreeStyle.vdx";
// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// Set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.LayoutStyle = LayoutStyle.CompactTree;
compactTreeOptions.EnlargePage = true;

// Set layout direction as DownThenRight and then save
compactTreeOptions.Direction = LayoutDirection.DownThenRight;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// Set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.DownThenLeft;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// Set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.RightThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// Set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.Direction = LayoutDirection.LeftThenDown;
diagram.Layout(compactTreeOptions);
diagram.Save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Автоматическая установка Visio Diagram**
 Aspose.Diagram API поддерживает автоматическую подгонку чертежа Visio. Эта функция помогает помещать внешние фигуры внутрь границ страницы Visio. Aspose.Diagram for .NET API имеет[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс, представляющий чертеж Visio.[ДиаграммаСохранитьОпции](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) Класс предоставляет свойство AutoFitPageToDrawingContent для автоматического подбора размера чертежа Visio.

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Создайте объект класса DiagramSaveOptions и передайте результирующий формат файла.
1. Установите свойство AutoFitPageToDrawingContent объекта DiagramSaveOptions.
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования автоматической подгонки**
В следующем примере кода показано, как автоматически подгонять фигуры в Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// Use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// Set Auto fit page property
options.AutoFitPageToDrawingContent = true;

// Save Visio diagram
diagram.Save(dataDir + "AutoFitShapesInVisio_out.vsdx", options);

{{< /highlight >}}
```
## **Работа с проектом VBA**
### **Изменить код модуля VBA в Visio Diagram**
 В этой статье показано, как автоматически изменить код модуля VBA с помощью Aspose.Diagram for .NET. Мы добавили[VbaModule](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [ВбаМодулеКоллекция](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [VbaProject](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) а также[ВбаПрожектРеференсКоллекшн](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) классы. Эти классы помогают получить контроль над проектом VBA. Разработчики могут извлекать и изменять код модуля VBA.
### **Изменить пример программирования кода модуля VBA**
Пожалуйста, проверьте этот пример кода:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdm", LoadFileFormat.VSDM);
// Extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// Save the Visio diagram
diagram.Save(dataDir + "ModifyVBAModule_out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **Удалить все макросы из Visio Diagram**
 Aspose.Diagram for .NET позволяет разработчикам удалять все макросы из Visio diagram. Свойство VbProjectData, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, позволяет удалить все макросы из чертежа Visio.
### **Пример программирования удаления всех макросов**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove all macros
diagram.VbProjectData = null;

// Save diagram
diagram.Save(dataDir + "RemoveMacrosFromVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vdxApp = null;
Visio.Document vdxDoc = null;
try
{
    // Create Visio Application Object
    vdxApp = new Visio.Application();

    // Make Visio Application Invisible
    vdxApp.Visible = false;

    // Create a new diagram
    vdxDoc = vdxApp.Documents.Add("");

    // Load Visio Stencil
    Visio.Documents visioDocs = vdxApp.Documents;
    Visio.Document visioStencil = visioDocs.OpenEx("Basic Shapes.vss",
        (short)Microsoft.Office.Interop.Visio.VisOpenSaveArgs.visOpenHidden);

    // Set active page
    Visio.Page visioPage = vdxApp.ActivePage;

    // Add a new rectangle shape
    Visio.Master visioRectMaster = visioStencil.Masters.get_ItemU(@"Rectangle");
    Visio.Shape visioRectShape = visioPage.Drop(visioRectMaster, 4.25, 5.5);
    visioRectShape.Text = @"Rectangle text.";

    // Add a new star shape
    Visio.Master visioStarMaster = visioStencil.Masters.get_ItemU(@"Star 7");
    Visio.Shape visioStarShape = visioPage.Drop(visioStarMaster, 2.0, 5.5);
    visioStarShape.Text = @"Star text.";

    // Add a new hexagon shape
    Visio.Master visioHexagonMaster = visioStencil.Masters.get_ItemU(@"Hexagon");
    Visio.Shape visioHexagonShape = visioPage.Drop(visioHexagonMaster, 7.0, 5.5);
    visioHexagonShape.Text = @"Hexagon text.";


    // Save diagram as VDX
    vdxDoc.SaveAs(dataDir + "CreatingDiagramWithVSTO_out.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}
            

{{< /highlight >}}
```
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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

// Create a new diagram
Diagram diagram = new Diagram(dataDir + "Basic Shapes.vss");

// Add a new rectangle shape
long shapeId = diagram.AddShape(4.25, 5.5, 2, 1, @"Rectangle", 0);
Shape shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Rectangle text."));

// Add a new star shape
shapeId = diagram.AddShape(2.0, 5.5, 2, 2, @"Star 7", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Star text."));

// Add a new hexagon shape
shapeId = diagram.AddShape(7.0, 5.5, 2, 2, @"Hexagon", 0);
shape = diagram.Pages[0].Shapes.GetShape(shapeId);
shape.Text.Value.Add(new Txt(@"Hexagon text."));

// Save the new diagram
diagram.Save(dataDir + "CreatingDiagramWithAspose_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_KnowledgeBase();

Visio.Application vsdApp = null;
Visio.Document vsdDoc = null;
try
{
    // Create Visio Application Object
    vsdApp = new Visio.Application();

    // Make Visio Application Invisible
    vsdApp.Visible = false;

    // Create a document object and load a diagram
    vsdDoc = vsdApp.Documents.Open(dataDir + "Drawing1.vsd");

    // Create page object to get required page
    Visio.Page page = vsdApp.ActivePage;

    // Create shape object to get required shape
    Visio.Shape shape = page.Shapes["Process1"];

    // Set shape text and text style
    shape.Text = "Hello World";
    shape.TextStyle = "CustomStyle1";

    // Set shape's position
    shape.get_Cells("PinX").ResultIU = 5;
    shape.get_Cells("PinY").ResultIU = 5;

    // Set shape's height and width
    shape.get_Cells("Height").ResultIU = 2;
    shape.get_Cells("Width").ResultIU = 3;

    // Save file as VDX
    vsdDoc.SaveAs(dataDir + "Drawing1.vdx");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message + "\nThis example will only work if you apply a valid Aspose License. You can purchase full license or get 30 day temporary license from http:// Www.aspose.com/purchase/default.aspx.");
}           

{{< /highlight >}}
```
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

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
try
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_KnowledgeBase();

    // Save the uploaded file as PDF
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Find a particular shape and update its properties
    foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
    {
        if (shape.Name.ToLower() == "process1")
        {
            shape.Text.Value.Clear();
            shape.Text.Value.Add(new Txt("Hello World"));

            // Find custom style sheet and set as shape's text style
            foreach (StyleSheet styleSheet in diagram.StyleSheets)
            {
                if (styleSheet.Name == "CustomStyle1")
                {
                    shape.TextStyle = styleSheet;
                }
            }

            // Set horizontal and vertical position of the shape
            shape.XForm.PinX.Value = 5;
            shape.XForm.PinY.Value = 5;

            // Set height and width of the shape
            shape.XForm.Height.Value = 2;
            shape.XForm.Width.Value = 3;
        }
    }

    // Save shape as VDX
    diagram.Save(dataDir + "UpdateShapePropsWithAspose_out.vdx", SaveFileFormat.VDX);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}

{{< /highlight >}}
```
