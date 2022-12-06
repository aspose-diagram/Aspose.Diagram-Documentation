---
title: Aspose.Diagram字体操作
type: docs
weight: 170
url: /zh/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram 允许开发人员设置用于在 Visio 图表中呈现的字体目录。本文介绍如何使用自定义目录中的字体。

{{% /alert %}} 
### **使用字体**
#### **Aspose.Diagram 在 Windows 上查找 TrueType 字体的位置**
Aspose.Diagram 搜索字体**Windows\字体**文件夹。此默认设置在大多数情况下都有效，因此仅在确实需要时才指定您自己的字体文件夹。
#### **如何明确指定字体文件夹**
Aspose.Diagram API 已公开 setFontDirs 方法[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类来指定字体文件夹，如下所述。

1. Diagram.setFontDirs 方法将字符串数组作为参数，因此开发人员可以使用此方法指定许多字体目录。

{{% alert color="primary" %}} 

使用上述方法指定字体文件夹时，我们建议在应用程序开始时设置字体位置，否则您可能会收到格式不正确的结果。

{{% /alert %}} {{% alert color="primary" %}} 

使用上述任何一种方法设置字体文件夹都不能确保 Aspose.Diagram API 不会在系统的字体文件夹等默认位置查找字体。

{{% /alert %}} 

演示如何设置 Aspose.Diagram 以在呈现或嵌入字体时在多个文件夹中查找 TrueType 字体。
#### **编程范例**
下面的代码示例演示了如何设置 Aspose.Diagram 以在呈现或嵌入字体时在多个文件夹中查找 TrueType 字体。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **在呈现过程中接收丢失字体和字体替换的通知**
Aspose.Diagram API 需要访问准确的字体才能将绘图正确呈现为 PDF 格式。如果所需字体在机器上不可用，则 Aspose.Diagram API 使用默认字体或机器上最接近的可用字体呈现该字体的任何实例，因为这种替换会改变呈现图形的外观，开发人员可能需要当缺少字体以及将用什么字体替换时收到通知。
#### **缺少字体的通知和字体替换编程示例**
在呈现期间通知字体替换：

1. 创建一个类来实现[警告回调](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. 将其传递给 PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback) 属性。

在保存图形的实例[警告回调](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)如果绘图存在任何潜在的保真度问题，则调用。在这种情况下，我们选择只处理字体替换的警告并将警告打印到屏幕上。下面的示例演示了如何通过使用接收字体替换通知[警告回调](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **实施 IWarningCallback**
最后一步是创建实现的类[警告回调](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)界面。此类将向控制台打印出任何字体替换警告。下面的示例演示了如何实现 IWarningCallback 以在文档保存期间收到有关任何字体替换的通知。



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
