---
title: 创建、更新、布局和自动调整形状
type: docs
weight: 10
url: /zh/net/create-update-layout-and-auto-fit-shapes/
description: 使用 C# Diagram API 在您的应用程序中使用 C# 在 Visio 文件中创建、更新和自动布局形状。包含 C# 代码示例的完整指南。
---
## **创建一个 Diagram**
 Aspose.Diagram for .NET 允许您从自己的应用程序中读取和创建 Microsoft Visio 图表，无需 Microsoft Office 自动化。创建新文档的第一步是创建一个 diagram。然后[添加形状和连接器](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)构建 diagram。使用默认构造函数[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类创建一个新的 diagram。
### **编程范例**
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
## **流程图样式的布局形状**
对于某些类型的连接图，例如流程图和网络图，您可以使用**布局形状**自动定位形状的功能。自动定位比手动将每个形状拖动到新位置更快。

例如，如果您正在更新一个大型流程图以包含一个新流程，您可以添加并连接构成该流程的形状，然后使用布局功能自动对更新后的绘图进行布局。

 Layout 方法，由[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class 在所有 diagram 的页面上布局形状和/或重新路由连接器。这个方法接受一个[布局选项](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)对象作为参数。使用 LayoutOptions 类公开的不同属性来自动布局形状。

下图显示了在应用自动布局之前，本文中的代码片段加载的 diagram。代码片段展示了如何应用[流程图布局](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)和[紧凑的树布局](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**来源 diagram。**

![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_1.png)

本文中的代码片段采用源代码 diagram 并对其应用多种类型的自动布局，将每种类型保存在单独的文件中。

|<p>**从下到上布局形状** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**从上到下布局形状** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**从左到右布局形状** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**从右到左布局形状** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_5.png)</p>|
以流程图样式布局形状：

1. 创建 Diagram 类的实例。
1. 创建 LayoutOptions 类的实例并设置 Flowchart 样式相关的属性。
1. 通过传递 LayoutOptions 调用 Diagram 类的 Layout 方法。
1. 调用Diagram类的Save方法写入Visio图。
### **流程图式编程示例**
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
### **以紧凑树样式布置形状**
紧凑的树形布局风格试图构建一个树形结构。它使用与[上面的例子](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)并保存为几种不同的紧凑树样式。

|<p>**紧凑的树形布局 - 向下和向右** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**紧凑的树形布局 - 右下** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
以紧凑的树形布局形状：

1. 创建一个实例[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)班级。
1. 创建 LayoutOptions 类的实例并设置紧凑树样式属性。
1. 通过传递 LayoutOptions 调用 Diagram 类的 Layout 方法。
1. 调用Diagram类的Save方法写入Visio文件。
#### **紧凑型树式编程示例**
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
## **自动适配 Visio Diagram**
 Aspose.Diagram API 支持自动适配Visio图。此功能操作有助于将外部形状带入 Visio 页面边界内。 Aspose.Diagram for .NET API 有[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)表示 Visio 绘图的类。这[图保存选项](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions)类公开 AutoFitPageToDrawingContent 属性以自动适应 Visio 绘图。

这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 创建 DiagramSaveOptions 类的对象并传递生成的文件格式。
1. 设置 DiagramSaveOptions 对象的 AutoFitPageToDrawingContent 属性。
1. 调用 Diagram 类对象的 Save 方法，并传递完整的文件路径和 DiagramSaveOptions 对象。
### **自动调整编程示例**
下面的示例代码显示了如何自动调整 Visio diagram 中的形状。

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
## **使用 VBA 项目**
### **Visio Diagram 修改VBA模块代码**
本文演示如何使用Aspose.Diagram for .NET自动修改一个VBA模块代码。我们添加了[Vba模块](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [Vba模块集合](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Vba项目](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [Vba项目参考](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference)和[VbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection)类。这些类有助于控制 VBA 项目。开发人员可以提取和修改 VBA 模块代码。
### **修改VBA模块代码编程范例**
请检查此代码示例：

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
### **从 Visio Diagram 中删除所有宏**
 Aspose.Diagram for .NET 允许开发人员从 Visio diagram 中删除所有宏。VbProjectData 属性，由[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)类，允许您从 Visio 绘图中删除所有宏。
### **删除所有宏编程示例**
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
## **使用 VSTO 创建一个新的 Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)允许开发人员创建和使用 Microsoft Office Visio 图表并将功能合并到他们的软件应用程序中。还有其他处理 Visio 文件的方法，最常见的是 Microsoft 自动化。不幸的是，这有一些局限性。 Aspose.Diagram功能强大，速度快，独立运行，无需Microsoft Office安装。

这篇迁移文章首先展示了如何使用[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/)接着[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)创建一个新的 diagram 并向其添加一些形状。你会注意到 Aspose.Diagram 代码比 VSTO 代码短。随意使用代码作为您自己开发的基础，并对其进行增强以满足您的需求。 VSTO 允许您使用 Microsoft Visio 文件进行编程。创建一个新的 diagram：

1. 创建一个 Visio 应用程序对象。
1. 使应用程序对象不可见。
1. 创建一个空的 diagram。
1. 添加来自 Visio 母版（模板）的形状。
1. 将文件另存为 VDX。
### **使用 VSTO 编程示例创建新的 Diagram**
{{% alert color="primary" %}}

使用 Visio = Microsoft.Office.Interop.Visio；
进口 Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**例子：**

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
## **用 Aspose.Diagram for .NET 创建一个新的 Diagram**
使用Aspose.Diagram API，开发者不需要在机器上安装Microsoft Office Visio，可以独立于Microsoft Office自动化工作。

创建一个新的 diagram：

1. 创建一个空的 diagram。
1. 添加来自 Visio 母版（模板）的形状。
1. 将文件另存为 VDX。
### **新的 Diagram 和 Aspose.Diagram for .NET 编程示例**
{{% alert color="primary" %}}

使用 Aspose.Diagram；
进口 Aspose.Diagram

{{% /alert %}}

例子：

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
## **更新形状属性**
使用 Microsoft Visio 图表时，用户可以更新形状属性，包括文本、样式、位置、高度和宽度。作为使用 Visio 文件的软件开发人员，您将被要求以编程方式执行此操作。好消息是，有可能使用 Microsoft 提供的 Visio 文件编程机制、VSTO，或使用[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

下面的主题显示了如何使用[VSTO](https://products.aspose.com/diagram/net/)和[Aspose.Diagram](https://products.aspose.com/diagram/net/)更新形状属性。下面的代码片段显示了如何更新 VSTO 和 Aspose.Diagram for .NET 的形状属性。请随意使用代码并将其应用于您的特定情况。
### **使用 VSTO 更新形状属性**
VSTO 允许您使用 Microsoft Visio 文件进行编程。要更新形状属性：

1. 创建一个 Visio 应用程序对象。
1. 使应用程序对象不可见。
1. 打开现有的 Visio VSD 文件。
1. 找到所需的形状。
1. 更新形状属性（文本、文本样式、位置和大小）。
1. 将文件另存为 VDX。
#### **使用 VSTO 编程示例更新形状属性**
{{% alert color="primary" %}}

使用 Visio = Microsoft.Office.Interop.Visio；
进口 Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**例子：**

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
### **使用 Aspose.Diagram for .NET 更新形状属性**
使用Aspose.Diagram API，开发者不需要在机器上使用Microsoft Office Visio，可以独立于Microsoft Office自动化工作。

要使用 Aspose.Diagram for .NET 更新形状属性：

1. 打开现有的 Visio VSD 文件。
1. 找到所需的形状。
1. 更新形状属性（文本、文本样式、位置和大小）。
1. 将文件另存为 VDX。
#### **使用 Aspose.Diagram for .NET 编程示例更新形状属性**
{{% alert color="primary" %}}

使用 Aspose.Diagram；
进口 Aspose.Diagram

{{% /alert %}}

**例子：**

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
