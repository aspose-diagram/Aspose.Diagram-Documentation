---
title: Работа с текстом
type: docs
weight: 90
url: /ru/net/working-with-text/
description: В этом разделе объясняется, как вставить текстовую фигуру или обновить текст фигуры с помощью Aspose.Diagram.
---
## **Вставьте текстовую фигуру на страницу Visio**
 Aspose.Diagram API позволяет разработчикам вставлять текст в любом месте страницы Visio. Для этого используется метод AddText класса[Страница](http://www.aspose.com/api/net/diagram/aspose.diagram/page) класс принимает параметры PinX, PinY, ширину, высоту и текст.
### **Вставка примера программирования формы текста**
Следующий фрагмент кода добавляет текстовую фигуру в Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Create a new diagram
Diagram diagram = new Diagram();
// Set parameters and add text to a Visio page
double PinX = 1, PinY = 1, Width = 1, Height = 1;                  
diagram.Pages[0].AddText(PinX, PinY, Width, Height, "Test text");
// Save diagram 
diagram.Save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Обновление Visio Форма текста**
 Так же как[создание диаграмм](/diagram/ru/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET позволяет работать с фигурами по-разному. В этой статье рассматривается, как получить доступ к тексту в фигурах и обновить его. Свойство Text, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, поддерживает объект Aspose.Diagram.Text. Свойство можно использовать для извлечения или обновления текста фигуры. Процесс обновления текста фигуры прост:

1. Загрузите diagram.
1. Найдите определенную форму.
1. Установите новый текст.
1. Сохраните номер diagram.
### **Обновить пример программирования текста формы**
Следующий фрагмент кода обновляет текст фигуры. Фигуры идентифицируются по их идентификаторам. Приведенные ниже сегменты кода ищут фигуру с именем process и идентификатором 1 и изменяют ее текст.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Применение встроенной или пользовательской таблицы стилей к фигуре Visio**
Microsoft Visio таблицы стилей хранят информацию о форматировании, которую можно применить к фигурам для единообразного внешнего вида. Aspose.Diagram for .NET позволяет применять таблицы стилей из приложения.

 Свойства TextStyle, FillStyle и LineStyle, предоставляемые[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс поддерживает[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) объект. Свойство можно использовать для получения информации о стиле и применения пользовательских стилей текста, линий и заливки к diagram.
### **Пользовательские стили в Microsoft Visio**
Чтобы применить пользовательские стили к фигурам в Microsoft Visio:

1. Откройте diagram в Microsoft Visio.
1.  Выбирать**Определить стили** от**Формат** меню (Visio 2007) или щелкните правой кнопкой мыши**Стили** в**Проводник по чертежам** окно и выберите**Определить стили** (Visio 2010).
1.  в**Определить стили** введите новое имя для пользовательской таблицы стилей. Например, CustomStyle1.
1.  Нажмите на**Текст**, **Линия** а также**Наполнять** кнопки для установки стилей текста, линий и заливки соответственно.
1.  Нажмите**ХОРОШО**.

После определения пользовательских таблиц стилей в Microsoft Visio используйте следующий код в приложении .NET, чтобы применить пользовательские стили к вашим фигурам. Обратите внимание, что приведенные ниже примеры кода вызывают пользовательскую таблицу стилей, определенную выше: вам необходимо знать имя и расположение применяемой таблицы. Чтобы применить пользовательские стили программно:

1. Загрузите diagram.
1. Найдите фигуру, к которой вы хотите применить стиль.
1. Загрузите таблицу стилей.
1. Применение стилей.
1. Сохраните номер diagram.
#### **Пример программирования применения пользовательских стилей**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
// Get page by name
Page page = vsdDiagram.Pages.GetPage("Flow 1");

Shape sourceShape = null;
// Find the shape to apply the style
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process")
    {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

// Find the required style sheet
foreach (StyleSheet styleSheet in vsdDiagram.StyleSheets)
{
    if (styleSheet.Name == "Basic")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    // Apply text style
    sourceShape.TextStyle = customStyleSheet;
    // Apply fill style
    sourceShape.FillStyle = customStyleSheet;
    // Apply line style
    sourceShape.LineStyle = customStyleSheet;
}

// Save changed diagram as VDX
vsdDiagram.Save(dataDir + "ApplyCustomStyleSheets_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **Применение разных стилей к каждому текстовому значению фигуры**
 Так же как[создание диаграмм](/diagram/ru/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET позволяет работать с фигурами по-разному. Эта статья поможет добавить несколько текстовых значений в фигуру и применить разные стили к каждому текстовому значению.

{{% alert color="primary" %}} 

Элемент Shape содержит элемент Text, который содержит символы текста и специальные элементы (cp, pp, tp и fld), обозначающие конец одного цикла и начало следующего. Элемент Char содержит атрибуты форматирования текста фигуры, такие как шрифт, цвет, стиль текста, регистр, положение относительно базовой линии и размер точек.

{{% /alert %}} 
### **Добавление текста и стилей фигуры**

|**Ввод diagram**|
|:- |
|![дело:изображение_альтернативный_текст](working-with-text_1.png)|


|**Diagram после добавления различных текстовых значений в фигуру с различным стилем для каждого текстового значения**|
|:- |
|![дело:изображение_альтернативный_текст](working-with-text_2.png)|
#### **Пример программирования добавления текста и стилей**
Следующий фрагмент кода добавляет текст фигуры и различные стили.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Clear shape text values and chars
shape.Text.Value.Clear();
shape.Chars.Clear();

// Mark character run and add text
shape.Text.Value.Add(new Cp(0));
shape.Text.Value.Add(new Txt("TextStyle_Regular\n"));
shape.Text.Value.Add(new Cp(1));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic\n"));
shape.Text.Value.Add(new Cp(2));
shape.Text.Value.Add(new Txt("TextStyle_Underline_Italic\n"));
shape.Text.Value.Add(new Cp(3));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic_Underline"));

// Add formatting characters
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());

// Set properties e.g. color, font, size and style etc.
shape.Chars[0].IX = 0;
shape.Chars[0].Color.Value = "#FF0000";
shape.Chars[0].Font.Value = 4;
shape.Chars[0].Size.Value = 0.22;
shape.Chars[0].Style.Value = StyleValue.Undefined;

// Set properties e.g. color, font, size and style etc.
shape.Chars[1].IX = 1;
shape.Chars[1].Color.Value = "#FF00FF";
shape.Chars[1].Font.Value = 4;
shape.Chars[1].Size.Value = 0.22;
shape.Chars[1].Style.Value = StyleValue.Bold | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[2].IX = 2;
shape.Chars[2].Color.Value = "#00FF00";
shape.Chars[2].Font.Value = 4;
shape.Chars[2].Size.Value = 0.22;
shape.Chars[2].Style.Value = StyleValue.Underline | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[3].IX = 3;
shape.Chars[3].Color.Value = "#3333FF";
shape.Chars[3].Font.Value = 4;
shape.Chars[3].Size.Value = 0.22;
shape.Chars[3].Style.Value = StyleValue.Bold | StyleValue.Italic | StyleValue.Underline;
// Save diagram
diagram.Save(dataDir + "ApplyFontOnText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Найти и заменить текст фигуры**
[Текст](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Класс позволяет редактировать текст фигуры. Метод Replace, представленный[Текст](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) class, поддержка изменения текста фигуры.
Примеры кода в этой статье находят и заменяют текст фигуры на странице.

|**Ввод diagram**|
|:- |
|![дело:изображение_альтернативный_текст](working-with-text_3.png)|


|**diagram после редактирования формы**|
|:- |
|![дело:изображение_альтернативный_текст](working-with-text_4.png)|
Процесс изменения текста фигуры:

1. Загрузите diagram.
1. Найдите конкретный текст фигуры.
1. Заменить текст этой формы
1. Сохраните номер diagram.
### **Пример программы поиска и замены текста**
Фрагменты кода ниже показывают, как изменить текст фигуры. Код перебирает формы страницы.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Prepare a collection old and new text
Dictionary<string, string> replacements = new Dictionary<string, string>();
replacements.Add("[[CompanyName]]", "Research Society of XYZ");
replacements.Add("[[EmployeeName]]", "James Bond");
replacements.Add("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");
replacements.Add("[[TimePeriod]]", DateTime.Now.AddYears(-1).ToString("dd/MMMM/yyyy") + " -- " + DateTime.Now.ToString("dd/MMMM/yyyy"));
replacements.Add("[[SubmissionDate]]", DateTime.Now.AddDays(-7).ToString("dd/MMMM/yyyy"));
replacements.Add("[[AmountReq]]", "$100,000");
replacements.Add("[[DateApproved]]", DateTime.Now.AddDays(1).ToString("dd/MMMM/yyyy"));

// Load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes of a page
foreach (Shape shape in page.Shapes)
{
    foreach (KeyValuePair<string, string> kvp in replacements)
    {
        foreach (FormatTxt txt in shape.Text.Value)
        {
            Txt tx = txt as Txt;
            if (tx != null && tx.Text.Contains(kvp.Key))
            {
                // Find and replace text of a shape
                tx.Text = tx.Text.Replace(kvp.Key, kvp.Value);
            }
        }
    }
}
// Save the diagram
diagram.Save(dataDir + "FindAndReplaceShapeText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Извлечь обычный текст со страницы Visio Diagram**
Aspose.Diagram API позволяет разработчикам извлекать обычный текст со страницы Visio diagram. Они также могут перебирать страницы Visio diagram, чтобы охватить весь текст Visio diagram.

 Microsoft Office Visio добавляет текст к фигурам.[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class содержит элемент с именем Text, который содержит символы текста и специальные элементы (cp, pp, tp и fld), отмечающие конец одного цикла и начало следующего.
### **Пример извлечения простого текста**
Следующий фрагмент кода перебирает формы страницы Visio и фильтрует обычный текст без информации о форматировании.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    // Iterate through the shapes
    foreach (Aspose.Diagram.Shape shape in page.Shapes)
    {
        // Extract plain text from the shape
        GetShapeText(shape);
    }
    // Display extracted text
    Console.WriteLine(text);
}
private static void GetShapeText(Aspose.Diagram.Shape shape)
{
    // Filter shape text
    if (shape.Text.Value.Text != "")
        text += Regex.Replace(shape.Text.Value.Text, "\\<.*?>", "");

    // For image shapes
    if (shape.Type == TypeValue.Foreign)
        text += (shape.Name);

    // For group shapes
    if (shape.Type == TypeValue.Group)
        foreach (Aspose.Diagram.Shape subshape in shape.Shapes)
        {
            GetShapeText(subshape);
        }
}

{{< /highlight >}}
```
