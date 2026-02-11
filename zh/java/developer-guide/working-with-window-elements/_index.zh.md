---
title: 使用窗口元素
type: docs
weight: 130
url: /zh/java/working-with-window-elements/
---
## **从 Visio 绘图中检索窗口元素**
主 Visio 应用程序窗口可以包含任何打开的 Visio 文件，就像现代网络浏览器允许在一个窗口中显示多个选项卡式网页一样。开发人员可以使用以下方法检索 Window 对象[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

这[窗口集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/windowcollection)对象代表一个列表[窗户](https://reference.aspose.com/diagram/java/com.aspose.diagram/window)绘图中可用的对象。 Windows 属性由 Diagram 类公开，支持 Aspose.Diagram.Window 对象的集合。此属性可用于检索窗口信息，即窗口 ID、类型、高度、宽度和状态。

**显示代码输出的控制台窗口。**

![待办事项：图片_替代_文本](http://i.imgur.com/zduARGh.png)
### **检索窗口元素编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveWindowElementsOfDiagram.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// iterate through the window elements
for (Window window :(Iterable<Window>) diagram.getWindows())
{
    System.out.println("ID: " + window.getID());
    System.out.println("Type: " + window.getWindowType());
    System.out.println("Window height: " + window.getWindowHeight());
    System.out.println("Window width: " + window.getWindowWidth());
    System.out.println("Window state: " + window.getWindowState());
}

{{< /highlight >}}

## **添加窗口元素到 Visio Diagram**
主 Visio 应用程序窗口可以包含任何打开的 Visio 文件，就像现代网络浏览器允许在一个窗口中显示多个选项卡式网页一样。开发人员现在可以在 Microsoft Visio 实例中添加一个新的 Window 对象，使用[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

Window 对象表示 Microsoft Visio 实例中打开的窗口。由 WindowCollection 类公开的 Add 方法允许添加一个新的 Window 对象。
### **添加窗口元素编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWindowElementInVisio.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// initialize window object
Window window = new Window();
// set window state
window.setWindowState(WindowStateValue.MAXIMIZED);
// set window height
window.setWindowHeight(500);
// set window width
window.setWindowWidth(500);
// set window type
window.setWindowType(WindowTypeValue.STENCIL);
// add window object
diagram.getWindows().add(window);

// save in any supported format
diagram.save(dataDir + "AddWindowElementInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **添加对动态网格和连接点的支持**
动态网格可帮助您相对于已放置在绘图中的形状垂直和水平放置新形状。关于连接点，一旦标记为勾选，就可以帮助我们在连接过程中看到连接点。我们可以使用实现这两个选项[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).
### **Visio 图纸中动态网格和连接点的支持**
Window 类提供 DynamicGridEnabled 和 ShowConnectionPoints 属性。这些属性可用于应用设置以支持动态网格和显示连接点选项。

**显示 Visio 中选项的 Visio 应用程序。**

![待办事项：图片_替代_文本](http://i.imgur.com/bxsJIwF.png)
#### **添加支持编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSupportOfVisualAids.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// check dynamic grid option
window.setDynamicGridEnabled(BOOL.TRUE);
// check connection points option
window.setShowConnectionPoints(BOOL.TRUE);
        
// save visio drawing
diagram.save(dataDir + "AddSupportOfVisualAids_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **显示和隐藏 Visio Diagram 的网格、标尺、参考线和分页符**
Microsoft Office Visio 有一对标尺、一个网格和两种类型的参考线和分页标志，用于查看每页上将打印的内容。开发人员可以使用这些设置[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).这些设置全局应用于单个页面。

Window 类提供 ShowGrid、ShowGuides、ShowRulers 和 ShowPageBreaks 属性。这些属性可用于应用设置以显示和隐藏网格、参考线、标尺和分页符。

**显示 Visio 中选项的 Visio 应用程序。**

![待办事项：图片_替代_文本](http://i.imgur.com/E0pvXbP.png)
### **编程范例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DisplayGridsRulersGuidesAndPageBreaks.class);     
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// get window object by index
Window window = diagram.getWindows().get(0);
// set visibility of grid
window.setShowGrid(BOOL.TRUE);
// set visibility of guides
window.setShowGuides(BOOL.TRUE);
// set visibility of rulers
window.setShowRulers(BOOL.TRUE);
// set visibility of page breaks
window.setShowPageBreaks(BOOL.TRUE);

// save diagram
diagram.save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

