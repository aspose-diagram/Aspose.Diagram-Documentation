---
title: Aspose.Diagram字体操作
type: docs
weight: 180
url: /zh/net/aspose-diagram-font-operations/
description: 本页介绍如何使用 Aspose.Diagram 库操作字体。
---
## **如何指定 TrueType 字体位置**
Aspose.Diagram 允许开发人员设置用于在 Visio 图表中呈现的字体目录。本文介绍如何使用自定义目录中的字体。
### **使用字体**
#### **Aspose.Diagram 在 Windows 上查找 TrueType 字体的位置**
Aspose.Diagram 搜索字体**Windows\字体**文件夹。此默认设置在大多数情况下都有效，因此仅在确实需要时才指定您自己的字体文件夹。
#### **如何明确指定字体文件夹**
Aspose.Diagram API 公开了 FontDirs 属性[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类来指定字体文件夹，如下所述。

1. Diagram.FontDirs 属性接受字符串数组，因此开发人员可以使用此方法指定许多字体目录。

{{% alert color="primary" %}} 

使用上述方法指定字体文件夹时，我们建议在应用程序开始时设置字体位置，否则您可能会收到格式不正确的结果。

{{% /alert %}} {{% alert color="primary" %}} 

使用上述任何一种方法设置字体文件夹都不能确保 Aspose.Diagram API 不会在系统的字体文件夹等默认位置查找字体。

{{% /alert %}} 
#### **编程范例**
下面的代码示例演示了如何设置 Aspose.Diagram 以在呈现或嵌入字体时在多个文件夹中查找 TrueType 字体。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Setting the custom font directories
diagram.FontDirs = fontDirs;

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "SpecifyFontLocation_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}

### **在呈现过程中接收丢失字体和字体替换的通知**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **缺少字体的通知和字体替换编程示例**
在呈现期间通知字体替换：

1. 创建一个类来实现[警告回调](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. 将其传递给 PdfSaveOptions.WarningCallback 属性。

在保存图形的实例[警告回调](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)如果绘图存在任何潜在的保真度问题，则调用。在这种情况下，我们选择只处理字体替换的警告并将警告打印到屏幕上。下面的示例演示了如何通过使用接收字体替换通知[警告回调](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **实施 IWarningCallback**
最后一步是创建实现的类[警告回调](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)界面。此类将向控制台打印出任何字体替换警告。下面的示例演示了如何实现 IWarningCallback 以在文档保存期间收到有关任何字体替换的通知。

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
