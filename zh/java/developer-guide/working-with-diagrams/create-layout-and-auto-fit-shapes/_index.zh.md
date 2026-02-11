---
title: 创建、布局和自动调整形状
type: docs
weight: 10
url: /zh/java/create-layout-and-auto-fit-shapes/
---
## **创建一个 Diagram**
 Aspose.Diagram for Java 允许您从自己的应用程序中读取和创建 Microsoft Visio 图表，无需 Microsoft Office 自动化。创建新文档的第一步是创建一个 diagram。然后[添加形状和连接器](/diagram/zh/java/add-and-connect-visio-shapes/)构建 diagram。使用默认构造函数[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类创建一个新的 diagram。
### **编程范例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **流程图样式的布局形状**
对于某些类型的连接图，例如流程图和网络图，您可以使用**布局形状**自动定位形状的功能。自动定位比手动将每个形状拖动到新位置更快。

例如，如果您正在更新一个大型流程图以包含一个新流程，您可以添加并连接构成该流程的形状，然后使用布局功能自动对更新后的绘图进行布局。

 Layout 方法，由[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class 在所有 diagram 的页面上布局形状和/或重新路由连接器。此方法接受 LayoutOptions 对象作为参数。使用 LayoutOptions 类公开的不同属性来自动布局形状。

下图显示了在应用自动布局之前，本文中的代码片段加载的 diagram。代码片段展示了如何应用[流程图布局](/diagram/zh/java/create-2c-layout-and-auto-fit-shapes/)和[紧凑的树布局](/diagram/zh/java/create-2c-layout-and-auto-fit-shapes/).

**来源 diagram。** 

![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_1.png)

本文中的代码片段采用源代码 diagram 并对其应用多种类型的自动布局，将每种类型保存在单独的文件中。

|<p>**从下到上布局形状** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**从上到下布局形状** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**从左到右布局形状** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**从右到左布局形状** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_5.png)</p>|
以流程图样式布局形状：

1. 创建 Diagram 类的实例。
1. 创建 LayoutOptions 类的实例并设置 Flowchart 样式相关的属性。
1. 通过传递 LayoutOptions 调用 Diagram 类的 Layout 方法。
1. 调用Diagram类的Save方法写入Visio图。
### **流程图式编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInFlowchartStyle.class);     

// load an existing Visio diagram
String fileName = "LayOutShapesInFlowchartStyle.vdx";
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setSpaceShapes(1f);
flowChartOptions.setEnlargePage(true);

// set layout direction as BottomToTop and then save
flowChartOptions.setDirection(LayoutDirection.BOTTOM_TO_TOP);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_btm_top.vdx", SaveFileFormat.VDX);

// set layout direction as TopToBottom and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_top_btm.vdx", SaveFileFormat.VDX);

// set layout direction as LeftToRight and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.LEFT_TO_RIGHT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_left_right.vdx", SaveFileFormat.VDX);

// set layout direction as RightToLeft and then save
diagram = new Diagram(dataDir + fileName);
flowChartOptions.setDirection(LayoutDirection.RIGHT_TO_LEFT);
diagram.layout(flowChartOptions);
diagram.save(dataDir + "sample_right_left.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **以紧凑树样式布置形状**
紧凑的树形布局风格试图构建一个树形结构。它使用与[上面的例子](/diagram/zh/java/create-2c-layout-and-auto-fit-shapes/)并保存为几种不同的紧凑树样式。

|<p>**紧凑的树形布局 - 向下和向右** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**紧凑的树形布局 - 右下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
以紧凑的树形布局形状：

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)班级。
1. 创建 LayoutOptions 类的实例并设置紧凑树样式属性。
1. 通过传递 LayoutOptions 调用 Diagram 类的 Layout 方法。
1. 调用Diagram类的Save方法写入Visio文件。
#### **紧凑型树式编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(LayOutShapesInCompactTreeStyle.class);
        
String fileName = "LayOutShapesInCompactTreeStyle.vdx";
// load an existing Visio diagram
Diagram diagram = new Diagram(dataDir + fileName);

// set layout options 
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setEnlargePage(true);

// set layout direction as DownThenRight and then save
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_right.vdx", SaveFileFormat.VDX);

// set layout direction as DownThenLeft and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_LEFT);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_down_left.vdx", SaveFileFormat.VDX);

// set layout direction as RightThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.RIGHT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_right_down.vdx", SaveFileFormat.VDX);

// set layout direction as LeftThenDown and then save
diagram = new Diagram(dataDir + fileName);
compactTreeOptions.setDirection(LayoutDirection.LEFT_THEN_DOWN);
diagram.layout(compactTreeOptions);
diagram.save(dataDir + "sample_left_down.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **自动适配 Visio Diagram**
Aspose.Diagram API 支持自动适配Visio图。此功能操作有助于将外部形状带入 Visio 页面边界内。

Aspose.Diagram for Java API 具有代表 Visio 绘图的 Diagram 类。 DiagramSaveOptions 类公开 AutoFitPageToDrawingContent 属性以自动适应 Visio 绘图。

这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 创建 DiagramSaveOptions 类的对象并传递生成的文件格式。
1. 设置 DiagramSaveOptions 对象的 AutoFitPageToDrawingContent 属性。
1. 调用 Diagram 类对象的 Save 方法，并传递完整的文件路径和 DiagramSaveOptions 对象。
### **自动调整编程示例**
下面的示例代码显示了如何自动调整 Visio diagram 中的形状。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AutoFitShapesInVisio.class);
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "BFlowcht.vsdx");

// use saving options
DiagramSaveOptions options = new DiagramSaveOptions(SaveFileFormat.VSDX);
// set Auto fit page property
options.setAutoFitPageToDrawingContent(true);

// save Visio diagram
diagram.save(dataDir + "AutoFitShapesInVisio_Out.vsdx", options);

{{< /highlight >}}
```
## **使用 VBA 项目**
### **Visio Diagram 修改VBA模块代码**
本文演示如何使用Aspose.Diagram for Java自动修改VBA模块代码。

我们添加了 VbaModule、VbaModuleCollection、VbaProject、VbaProjectReference 和 VbaProjectReferenceCollection 类。这些类有助于控制 VBA 项目。开发人员可以提取和修改 VBA 模块代码。
### **修改VBA模块代码编程范例**
请检查此代码示例：

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// load an existing Visio diagram
String dataDir = Utils.getDataDir(ModifyVBAModuleCode.class);
InputStream input = new FileInputStream(dataDir + "macro.vsdm");
Diagram diagram = new Diagram(input);
// extract VBA project
VbaProject v = diagram.getVbaProject();
// Iterate through the modules and modify VBA macro code
for (int i = 0; i < diagram.getVbaProject().getModules().getCount(); i++) {
	VbaModule module = diagram.getVbaProject().getModules().get(i);
	String code = module.getCodes();
	if (code.contains("This is test message."))
		code = code.replace("This is test message.", "This is Aspose.Diagram message.");
	module.setCodes(code);
}
// save the Visio diagram
diagram.save(dataDir + "out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
```
### **从 Visio Diagram 中删除所有宏**
Aspose.Diagram for Java 允许开发人员从 Visio diagram 中删除所有宏。

JavaProjectData 属性，由[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类，允许您从 Visio 绘图中删除所有宏。
### **删除所有宏编程示例**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RemoveMacrosFromVisio.class);  
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// remove all macros
diagram.setVbProjectData(null);

// Save diagram
diagram.save(dataDir + "RemoveMacrosFromVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
