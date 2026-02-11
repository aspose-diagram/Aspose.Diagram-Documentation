---
title: 使用窗口元素
type: docs
weight: 100
url: /zh/net/working-with-window-elements/
description: 本节用Aspose.Diagram说明visio窗口元素的get属性。
---
## **从 Visio 绘图中检索窗口元素**
主 Visio 应用程序窗口可以包含任何打开的 Visio 文件，就像现代网络浏览器允许在一个窗口中显示多个选项卡式网页一样。开发人员可以使用以下方法检索 Window 对象[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

这[窗口集合](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection)对象代表一个列表[窗户](http://www.aspose.com/api/net/diagram/aspose.diagram/window)绘图中可用的对象。 Windows 属性由 Diagram 类公开，支持 Aspose.Diagram.Window 对象的集合。此属性可用于检索窗口信息，即窗口 ID、类型、高度、宽度和状态。
### **检索窗口元素编程示例**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}

## **添加窗口元素到 Visio Diagram**
主 Visio 应用程序窗口可以包含任何打开的 Visio 文件，就像现代网络浏览器允许在一个窗口中显示多个选项卡式网页一样。开发人员现在可以在 Microsoft Visio 实例中添加一个新的 Window 对象，使用[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

这[窗户](http://www.aspose.com/api/net/diagram/aspose.diagram/window) object 表示 Microsoft Visio 实例中打开的窗口。这[添加](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add)方法，由[窗口集合](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection)类，允许添加一个新的 Window 对象。
### **添加窗口元素编程示例**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **添加对动态网格和连接点的支持**
动态网格可帮助您相对于已放置在绘图中的形状垂直和水平放置新形状。关于连接点，一旦标记为勾选，就可以帮助我们在连接过程中看到连接点。我们可以使用实现这两个选项[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Visio 图纸中动态网格和连接点的支持**
这[窗户](http://www.aspose.com/api/net/diagram/aspose.diagram/window)类提供 DynamicGridEnabled 和 ShowConnectionPoints 属性。这些属性可用于应用设置以支持动态网格和显示连接点选项。
#### **添加支持编程示例**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **显示和隐藏 Visio Diagram 的网格、标尺、参考线和分页符**
Microsoft Office Visio 有一对标尺、一个网格和两种类型的参考线和分页标志，用于查看每页上将打印的内容。开发人员可以使用这些设置[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).这些设置全局应用于单个页面。

这[窗户](http://www.aspose.com/api/net/diagram/aspose.diagram/window)类提供 ShowGrid、ShowGuides、ShowRulers 和 ShowPageBreaks 属性。这些属性可用于应用设置以显示和隐藏网格、参考线、标尺和分页符。
### **编程范例**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

