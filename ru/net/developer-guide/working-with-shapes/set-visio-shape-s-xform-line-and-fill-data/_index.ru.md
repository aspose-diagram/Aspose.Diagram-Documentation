---
title: Установите Visio XForm, линии и данные заливки фигуры
type: docs
weight: 20
url: /ru/net/set-visio-shape-s-xform-line-and-fill-data/
description: В этом разделе объясняется, как установить стиль фигуры, включая ее данные линии и данные заливки с помощью Aspose.Diagram.
---
## **Настройка данных XForm**
 Элемент XForm является частью схемы XML Microsoft Visio. XForm указывает положение фигуры, например ширину, высоту, поворот и была ли фигура перевернута.[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) имущество, выставленное[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class поддерживает объект Aspose.Diagram.XForm. Свойство XForm можно использовать для извлечения или обновления данных XForm фигуры. Примеры кода в этой статье изменяют значения XForm PinX (координата X) и PinY (координата Y) для перемещения фигур на странице.

Процесс обновления данных XForm:

1. Загрузите diagram.# Найдите конкретную фигуру.# Обновите данные XForm фигуры.
1. Сохраните номер diagram.
### **Образец программирования**
Фрагмент кода ниже показывает, как обновить данные XForm фигуры. Код ищет процесс имен фигур с идентификатором фигуры 1 и устанавливает его координаты X и Y равными 5.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.XForm.PinX.Value = 5;
        shape.XForm.PinY.Value = 5;
    }
}
// Save diagram
diagram.Save(dataDir + "SetXFormdata_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Установить Visio данные линии фигуры**
Формы можно форматировать несколькими способами. В этой статье показано, как указать атрибуты линии.

Microsoft Visio позволяет пользователям форматировать строки различными способами. Aspose.Diagram for .NET поддерживает:

- Вес: толщина линии.
- Цвет: установите цвет линии фигуры.
- Прозрачность цвета линии: установите прозрачность цвета линии фигуры в процентах.
- Узор: определяет, является ли линия сплошной, пунктирной или имеет другой узор.
- Скругление: радиус углов.
- Начальная и конечная стрелки: указано, есть ли в строке стрелки.
- Начальный и конечный размеры стрелок: задайте размеры стрелок.
- Заглушка: закругление линии заканчивается.
### **Измените цвет линии, толщину, тип штриха, прозрачность, округление, тип стрелки и размер стрелки границы фигуры.**
[Линия](http://www.aspose.com/api/net/diagram/aspose.diagram/line) имущество, выставленное[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class, поддерживает объект Aspose.Diagram.Line. Это свойство можно использовать для извлечения или обновления данных линии фигуры.
#### **Образец программирования линейных данных**
Следующий фрагмент кода обновляет линейные данные shape.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// Get the page by its name
Aspose.Diagram.Page page1 = diagram.Pages.GetPage("Page-1");
// Get shape by its ID
Aspose.Diagram.Shape shape = page1.Shapes.GetShape(1);
// Set line dash type by index
shape.Line.LinePattern.Value = 4;
// Set line weight, defualt in inch
shape.Line.LineWeight.Value = 2;
// Set color of the shape's line
shape.Line.LineColor.Ufe.F = "RGB(95,108,53)";
// Set line rounding, default in inch
shape.Line.Rounding.Value = 0.3125;
// Set line caps
shape.Line.LineCap.Value = BOOL.True;
// Set line color transparency in percent
shape.Line.LineColorTrans.Value = 50;

/* add arrows to the connector or curve shapes */
// Select arrow type by index
shape.Line.BeginArrow.Value = 4;
shape.Line.EndArrow.Value = 4;
// Set arrow size 
shape.Line.BeginArrowSize.Value = ArrowSizeValue.Large;
shape.Line.EndArrowSize.Value = ArrowSizeValue.Large;

// Save the Visio
diagram.Save(dataDir + "SetLineData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Установить Visio данные заполнения фигуры**
 Формы можно форматировать несколькими способами. В этом разделе описывается, как задать заливку фигуры. Microsoft Office Visio позволяет пользователям форматировать заливки различными способами.[Наполнять](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) класс Aspose.Diagram for .NET API поддерживает настройку:

- Цвета фона и переднего плана.
- Прозрачность.
- Заполнение узорами.
- Тени.
### **Установка значений заполнения**
 Свойство Fill, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс, поддерживает[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) объект. Свойство Fill можно использовать для извлечения или обновления данных заполнения фигуры.
#### **Образец программирования данных заполнения**
Следующий фрагмент кода обновляет данные заполнения фигуры. Код ищет фигуру с именем прямоугольник с идентификатором фигуры 1 и устанавливает цвета фона и переднего плана заливки.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetFillData.vsd");

// Find a particular shape and update its XForm
foreach (Aspose.Diagram.Shape shape in diagram.Pages[0].Shapes)
{
    if (shape.NameU.ToLower() == "rectangle" && shape.ID == 1)
    {
        shape.Fill.FillBkgnd.Value = diagram.Pages[1].Shapes[0].Fill.FillBkgnd.Value;
        shape.Fill.FillForegnd.Value = "#ebf8df";
    }
}
// Save diagram
diagram.Save(dataDir + "SetFillData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
### **Получить унаследованные данные заполнения формы Visio**
 Фигуры Visio могут наследовать родительский стиль и основную фигуру. Разработчики могут получить или установить наследуемые данные заполнения фигуры Visio. Свойство InheritFill, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class содержит значения форматирования заливки для фигуры, наследуемой родительским стилем и основной фигурой.
#### **Пример программирования извлечения унаследованных данных заполнения**
Следующий фрагмент кода извлекает унаследованные данные заливки фигуры. Пожалуйста, проверьте этот пример кода:

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get the fill formatting values
Console.WriteLine(shape.InheritFill.FillBkgnd.Value);
Console.WriteLine(shape.InheritFill.FillForegnd.Value);
Console.WriteLine(shape.InheritFill.FillPattern.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwObliqueAngle.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetX.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwOffsetY.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwScaleFactor.Value);
Console.WriteLine(shape.InheritFill.ShapeShdwType.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgnd.Value);
Console.WriteLine(shape.InheritFill.ShdwBkgndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwForegnd.Value);
Console.WriteLine(shape.InheritFill.ShdwForegndTrans.Value);
Console.WriteLine(shape.InheritFill.ShdwPattern.Value);

{{< /highlight >}}
```
