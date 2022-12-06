---
title: 创建、布局和自动调整形状
type: docs
weight: 10
url: /zh/python-java/create-layout-and-auto-fit-shapes/
---
## **创建一个 Diagram**
Aspose.Diagram for Python via Java 允许您从自己的应用程序中读取和创建 Microsoft Visio 图表，无需 Microsoft Office 自动化。创建新文档的第一步是创建一个 diagram。然后[添加形状和连接器](/diagram/zh/python-java/add-and-connect-visio-shapes/)构建 diagram。使用 Diagram 类的默认构造函数创建一个新的 diagram。
### **编程范例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-CreateDiagram.py" >}}
## **流程图样式的布局形状**
对于某些类型的连接图，例如流程图和网络图，您可以使用**布局形状**自动定位形状的功能。自动定位比手动将每个形状拖动到新位置更快。

例如，如果您正在更新一个大型流程图以包含一个新流程，您可以添加并连接构成该流程的形状，然后使用布局功能自动对更新后的绘图进行布局。

Diagram 类公开的 Layout 方法布局形状和/或重新路由所有 diagram 页面上的连接器。此方法接受 LayoutOptions 对象作为参数。使用 LayoutOptions 类公开的不同属性来自动布局形状。

下图显示了在应用自动布局之前，本文中的代码片段加载的 diagram。代码片段展示了如何应用流程图布局和紧凑的树布局。

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
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInFlowchartStyle.py" >}}
### **以紧凑树样式布置形状**
紧凑的树形布局风格试图构建一个树形结构。它使用与上面示例相同的输入文件，并保存为几种不同的紧凑树样式。

|<p>**紧凑的树形布局 - 向下和向右** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**紧凑的树形布局 - 右下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**紧凑的树形布局 - 左下** </p><p>![待办事项：图片_替代_文本](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
以紧凑的树形布局形状：

1. 创建 Diagram 类的实例。
1. 创建 LayoutOptions 类的实例并设置紧凑树样式属性。
1. 通过传递 LayoutOptions 调用 Diagram 类的 Layout 方法。
1. 调用Diagram类的Save方法写入Visio文件。
#### **紧凑型树式编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInCompactTreeStyle.py" >}}
## **自动适配 Visio Diagram**
Aspose.Diagram API 支持自动适配Visio图。此功能操作有助于将外部形状带入 Visio 页面边界内。

Aspose.Diagram for Python via Java API 具有代表 Visio 绘图的 Diagram 类。 DiagramSaveOptions 类公开 AutoFitPageToDrawingContent 属性以自动适应 Visio 绘图。

这个例子的工作原理如下：

1. 创建 Diagram 类的对象。
1. 创建 DiagramSaveOptions 类的对象并传递生成的文件格式。
1. 设置 DiagramSaveOptions 对象的 AutoFitPageToDrawingContent 属性。
1. 调用 Diagram 类对象的 Save 方法，并传递完整的文件路径和 DiagramSaveOptions 对象。
### **自动调整编程示例**
下面的示例代码显示了如何自动调整 Visio diagram 中的形状。

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-AutoFitShapesInVisio.py" >}}
## **使用 VBA 项目**
### **Visio Diagram 修改VBA模块代码**
本文演示如何通过Java为Python自动使用Aspose.Diagram修改一个VBA模块代码。

我们添加了 VbaModule、VbaModuleCollection、VbaProject、VbaProjectReference 和 VbaProjectReferenceCollection 类。这些类有助于控制 VBA 项目。开发人员可以提取和修改 VBA 模块代码。
### **修改VBA模块代码编程范例**
请检查此代码示例：

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-ModifyVBAModuleCode.py" >}}
### **从 Visio Diagram 中删除所有宏**
Aspose.Diagram for Python via Java 允许开发人员从 Visio diagram 中删除所有宏。

Diagram 类公开的 JavaProjectData 属性允许您从 Visio 绘图中删除所有宏。
### **删除所有宏编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-RemoveMacrosFromVisio.py" >}}
