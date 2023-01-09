---
title: 介绍
type: docs
weight: 10
url: /zh/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio 将有关对 diagram 采取的操作的信息保存在文件中。例如，文档创建的时间和日期，最后一次编辑、打印或保存的时间，都与文件一起保存。有关 Microsoft Visio 创建和最后编辑文件的版本的信息也被保存。

本文介绍了如何检索该信息。

{{% /alert %}} 
## **获取Aspose.Diagram for Java库的版本**
getVersion() 方法由[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)类和由公开的 getBuildNumberCreated() 方法[文档属性](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)类用于确定用于创建文档的 Microsoft Visio 实例的版本和完整构建号。
### **Determining the Version of Microsoft Visio 创建、编辑和保存文档**
getBuildNumberEdited() 方法由[文档属性](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)类用于确定用于编辑文档的 Microsoft Visio 实例的完整构建号。

getTimeCreated()、getTimeEdited()、getTimePrinted() 和 getTimeSaved() 方法由[文档属性](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)class 用于确定 Microsoft Visio 文档的创建、最后编辑、最后打印和最后保存的时间。

您还可以设置这些属性来更改文件中的信息。

下面的代码示例显示了如何检索有关文件创建者以及文件创建、编辑、打印和保存时间的信息。

**控制台窗口中的代码输出** 

![待办事项：图片_替代_文本](introduction_1.png)
#### **编程范例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **写作 Microsoft Visio 文档摘要信息**
Microsoft Visio 允许您定义许多文档摘要信息属性，以帮助您和您的同事识别 diagram。摘要属性，例如标题、主题、作者和描述，使文件在搜索时更容易找到，在浏览时更容易识别文件。

这[文档属性](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)类公开了一些属性来设置或获取 Microsoft Visio diagram 的摘要信息。 Aspose.Diagram for Java 可以更新图纸汇总信息，然后将图纸文件写回VDX。

{{% alert color="primary" %}} 

请注意，您不能针对**应用**和**制作人**字段，因为 Aspose Ltd. 和 Aspose.Diagram for Java xxx 将针对这些字段显示。

{{% /alert %}} 
### **写作 Microsoft Visio 文档摘要信息**
要更新现有 VDX 或 VSD 文件的图纸摘要信息：

1. 创建一个实例[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)班级。
1. 设置 Diagram.getDocumentProps() 方法公开的属性，以定义 Visio 绘图文件的摘要信息。
1. 调用Diagram类的save()方法将Visio绘图文件写入VDX。

查看摘要信息：

1. 在Microsoft Visio打开输出VDX文件。
1. 选择**信息**来自**文件**菜单。

**显示更新的摘要信息的信息对话框** 

![待办事项：图片_替代_文本](introduction_2.png)
#### **编程范例**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **检测 Visio 文件的格式**
使用[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API，开发者可以在打开Visio文件前检测其格式，因为文件扩展名并不能保证文件内容是合适的。
### **检测格式编程示例**
以下示例代码说明了如何检测文件格式（使用文件路径或流）并检查其扩展名。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **从 InputStream 检测 Visio 文件的格式**
使用 Aspose.Diagram for Java API，开发人员可以通过传递输入流来检测 Visio 文件的格式。 FileFormatUtil 类的 detectFileFormat 方法可用于实现此目的。
### **从 InputStream 编程示例中检测格式**
以下示例代码说明了如何使用输入流检测文件格式。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
