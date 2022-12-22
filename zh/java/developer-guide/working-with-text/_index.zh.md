---
title: 使用文本
type: docs
weight: 120
url: /zh/java/working-with-text/
---
## **在 Visio 页面中插入一个文本形状**
Aspose.Diagram API 允许开发人员在 Visio 页面的任意位置插入文本形状。为实现这一点，[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)类采用 PinX、PinY、宽度、高度和文本参数。
### **插入文本形状编程示例**
下面这段代码在 Visio diagram 中添加了一个文本形状。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-InsertTextShape-InsertTextShape.java" >}}
## **更新 Visio 形状文本**
也[创建图表](/diagram/zh/java/load-or-create-a-visio-drawing/)Aspose.Diagram for Java 让您以不同的方式处理形状。本文着眼于如何访问和更新形状中的文本。

 Text 属性，由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类，支持 Aspose.Diagram.Text 对象。该属性可用于检索或更新形状的文本。

**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/6aEp7h0.png)

**Diagram 中心形状中的文本从 Process 更改为 New Text** 

![待办事项：图片_替代_文本](http://i.imgur.com/o977cxw.png)

更新形状文本的过程很简单：

1. 加载一个 diagram。
1. 找到一个特定的形状。
1. 设置新文本。
1. 保存 diagram。
### **更新形状文本编程示例**
以下代码段更新形状的文本。形状由它们的 ID 标识。下面的代码段查找名为 process 且 ID 为 1 的形状并更改其文本。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-UpdateShapeText-UpdateShapeText.java" >}}
## **将内置或自定义样式表应用于 Visio 形状**
Microsoft Visio 样式表存储格式信息，这些信息可应用于形状以获得一致的外观和感觉。 Aspose.Diagram for Java 允许您从应用程序内部应用样式表。

 TextStyle、FillStyle 和 LineStyle 属性由[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类支持[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet)目的。该属性可用于检索样式信息并将自定义文本、线条和填充样式应用于 diagram。

**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/feV1x2N.png)

**应用定义文本、线条和填充样式的自定义样式表后的 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/Xk9W0wN.png)
### **Microsoft Visio 中的自定义样式**
将自定义样式应用于 Microsoft Visio 中的形状：

1. 在Microsoft Visio开一个diagram。
1. 选择**定义样式**来自**格式**菜单 (Visio 2007)，或右键单击**样式**在里面**绘图资源管理器**窗口，然后选择**定义样式** (Visio 2010).
1. 在里面**定义样式**对话框，为您的自定义样式表键入一个新名称。例如，CustomStyle1。
1. 点击**文本**, **线**和**充满**按钮分别设置文本、线条和填充样式。
1. 点击**好的**.

在 Microsoft Visio 中定义自定义样式表后，在 Java 应用程序中使用以下代码将自定义样式应用于您的形状。请注意，下面的代码示例调用上面定义的自定义样式表：您需要知道您应用的表单的名称和位置。

要以编程方式应用自定义样式：

1. 加载一个 diagram。
1. 找到要应用样式的形状。
1. 加载样式表。
1. 应用样式。
1. 保存 diagram。
#### **应用自定义样式编程示例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.java" >}}
## **对形状的每个文本值应用不同的样式**
也[创建图表](/diagram/zh/java/load-or-create-a-visio-drawing/)Aspose.Diagram for Java 让您以不同的方式处理形状。本文有助于将多个文本值添加到一个形状，并对每个文本值应用不同的样式。

{{% alert color="primary" %}} 

Shape 元素包含一个名为 Text 的元素，其中包含文本字符和标记一次运行结束和下一次运行开始的特殊元素（cp、pp、tp 和 fld）。 Char 元素包含形状文本的格式化属性，例如字体、颜色、文本样式、大小写、相对于基线的位置和磅值。

{{% /alert %}} 
### **添加形状文本和样式**
**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/ZqgQPQC.png)

**Diagram 在将各种文本值添加到每个文本值上具有不同样式的形状之后** 

![待办事项：图片_替代_文本](http://i.imgur.com/7UWhFbU.png)
#### **添加文本和样式编程示例**
下面的一段代码添加了一个形状的文本和不同的样式。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-ApplyFontOnText-ApplyFontOnText.java" >}}
## **查找和替换形状的文本**
这[文本](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt)类允许您编辑形状的文本。 Replace 方法，由[文本](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt)类，支持更改形状的文本。
本文中的代码示例查找并替换页面上形状的文本。

**输入 diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/lW5xaP0.png)


**形状编辑后的diagram** 

![待办事项：图片_替代_文本](http://i.imgur.com/m33W1Tk.png)

更改形状文本的过程：

1. 加载一个 diagram。
1. 查找形状的特定文本。
1. 替换此形状的文本
1. 保存 diagram。
### **查找和替换文本编程示例**
下面的代码片段显示了如何修改形状的文本。代码遍历页面的形状。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.java" >}}
## **从 Visio Diagram 页面中提取纯文本**
Aspose.Diagram API 允许开发人员从 Visio diagram 页面中提取纯文本。他们还可以遍历 Visio diagram 页以覆盖整个 Visio diagram 文本。

 Microsoft Office Visio 将文本添加到形状中。这[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类包含一个名为 Text 的元素，该元素包含文本字符和标记一次运行结束和下一次运行开始的特殊元素（cp、pp、tp 和 fld）。
### **提取纯文本编程示例**
以下代码段遍历 Visio Page 的形状并过滤没有格式信息的纯文本。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.java" >}}
