---
title: 使用文本
type: docs
weight: 90
url: /zh/net/working-with-text/
description: 本节介绍如何使用 Aspose.Diagram 插入文本形状或更新形状的文本。
---
## **在 Visio 页面中插入一个文本形状**
 Aspose.Diagram API 允许开发人员在 Visio 页面的任意位置插入文本形状。为实现这一点，AddText 方法[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类采用 PinX、PinY、宽度、高度和文本参数。
### **插入文本形状编程示例**
下面这段代码在 Visio diagram 中添加了一个文本形状。

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
## **更新 Visio 形状文本**
也[创建图表](/diagram/zh/net/load-or-create-a-visio-drawing/) Aspose.Diagram for .NET 让您以不同的方式处理形状。本文着眼于如何访问和更新形状中的文本。 Text 属性，由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类，支持 Aspose.Diagram.Text 对象。该属性可用于检索或更新形状的文本。更新形状文本的过程很简单：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 设置新文本。
1. 保存 diagram。
### **更新形状文本编程示例**
以下代码段更新形状的文本。形状由它们的 ID 标识。下面的代码段查找名为 process 且 ID 为 1 的形状并更改其文本。

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
## **将内置或自定义样式表应用于 Visio 形状**
Microsoft Visio 样式表存储格式信息，这些信息可应用于形状以获得一致的外观和感觉。 Aspose.Diagram for .NET 允许您从应用程序内部应用样式表。

 TextStyle、FillStyle 和 LineStyle 属性由[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类支持[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet)目的。该属性可用于检索样式信息并将自定义文本、线条和填充样式应用于 diagram。
### **Microsoft Visio 中的自定义样式**
将自定义样式应用于 Microsoft Visio 中的形状：

1. 在Microsoft Visio开一个diagram。
1. 选择**定义样式**来自**格式**菜单 (Visio 2007)，或右键单击**样式**在里面**绘图资源管理器**窗口，然后选择**定义样式** (Visio 2010).
1. 在里面**定义样式**对话框，为您的自定义样式表键入一个新名称。例如，CustomStyle1。
1. 点击**文本**, **线**和**充满**按钮分别设置文本、线条和填充样式。
1. 点击**好的**.

在 Microsoft Visio 中定义自定义样式表后，在 .NET 应用程序中使用以下代码将自定义样式应用于您的形状。请注意，下面的代码示例调用上面定义的自定义样式表：您需要知道您应用的表单的名称和位置。要以编程方式应用自定义样式：

1. 加载一个 diagram。
1. 找到要应用样式的形状。
1. 加载样式表。
1. 应用样式。
1. 保存 diagram。
#### **应用自定义样式编程示例**
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
## **对形状的每个文本值应用不同的样式**
也[创建图表](/diagram/zh/net/load-or-create-a-visio-drawing/)Aspose.Diagram for .NET 让您以不同的方式处理形状。本文有助于将多个文本值添加到一个形状，并对每个文本值应用不同的样式。

{{% alert color="primary" %}} 

Shape 元素包含一个名为 Text 的元素，其中包含文本字符和标记一次运行结束和下一次运行开始的特殊元素（cp、pp、tp 和 fld）。 Char 元素包含形状文本的格式化属性，例如字体、颜色、文本样式、大小写、相对于基线的位置和磅值。

{{% /alert %}} 
### **添加形状文本和样式**

|**输入 diagram**|
|:- |
|![待办事项：图片_替代_文本](working-with-text_1.png)|


|**Diagram 在将各种文本值添加到每个文本值上具有不同样式的形状之后**|
|:- |
|![待办事项：图片_替代_文本](working-with-text_2.png)|
#### **添加文本和样式编程示例**
下面的一段代码添加了一个形状的文本和不同的样式。

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
## **查找和替换形状的文本**
这[文本](http://www.aspose.com/api/net/diagram/aspose.diagram/txt)类允许您编辑形状的文本。 Replace 方法，由[文本](http://www.aspose.com/api/net/diagram/aspose.diagram/txt)类，支持更改形状的文本。
本文中的代码示例查找并替换页面上形状的文本。

|**输入 diagram**|
|:- |
|![待办事项：图片_替代_文本](working-with-text_3.png)|


|**形状编辑后的diagram**|
|:- |
|![待办事项：图片_替代_文本](working-with-text_4.png)|
更改形状文本的过程：

1. 加载一个 diagram。
1. 查找形状的特定文本。
1. 替换此形状的文本
1. 保存 diagram。
### **查找和替换文本编程示例**
下面的代码片段显示了如何修改形状的文本。代码遍历页面的形状。

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
## **从 Visio Diagram 页面中提取纯文本**
Aspose.Diagram API 允许开发人员从 Visio diagram 页面中提取纯文本。他们还可以遍历 Visio diagram 页以覆盖整个 Visio diagram 文本。

 Microsoft Office Visio 将文本添加到形状中。这[形状](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)类包含一个名为 Text 的元素，该元素包含文本字符和标记一次运行结束和下一次运行开始的特殊元素（cp、pp、tp 和 fld）。
### **提取纯文本编程示例**
以下代码段遍历 Visio Page 的形状并过滤没有格式信息的纯文本。

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
