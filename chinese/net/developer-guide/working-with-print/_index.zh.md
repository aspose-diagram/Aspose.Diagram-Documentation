---
title: 使用打印
type: docs
weight: 80
url: /zh/net/working-with-print/
description: This section explains how to print a document via XpsPrint with Aspose.Diagram.
---
## **How to Print a Document on a Server via the XpsPrint API**
This article can be useful to anyone who wants to submit an XPS document to the unmanaged XpsPrint API from a .NET application. But the main goal if this article is to show how to print a diagram from an ASP.NET or Windows Service application using Aspose.Diagram and the XpsPrint API.
### **问题**
当您开发 .NET 应用程序并需要生成一些打印输出时，您可以使用 System.Drawing.Printing 命名空间中的类或 WPF 类。但是，事实证明，如果您开发 ASP.NET 或 Windows 服务应用程序，那么您的打印选项将受到严重限制，因为 Microsoft 建议不要使用这些方法。有关详细信息，请参阅下面的链接。

<http://support.microsoft.com/kb/324565>

服务不支持使用 .NET Framework 打印类。这包括 ASP 页面，它们通常在服务器服务的上下文中运行。

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

不支持在 Windows 服务或 ASP.NET 应用程序或服务中使用 System.Drawing.Printing 命名空间中的类。尝试从其中一种应用程序类型中使用这些类可能会产生意想不到的问题，例如服务性能下降和运行时异常。

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

不支持使用 WPF 构建 Windows 服务。由于 WPF 是一种表示技术，因此 Windows 服务需要适当的权限才能执行涉及用户交互的可视化操作。如果 Windows 服务没有适当的权限，可能会出现意想不到的结果。

The Document object provides a family of the Print methods to print documents and these methods print via the .NET printing classes defined in the System.Drawing.Printing namespace. There are many customers of Aspose.Diagram who use this printing method in their server-side applications without any problems, but there is a way to comply with Microsoft’s recommendations and it is described in this article.
### **解决方案**
根据 Microsoft 打印文档的正确方法是使用非托管 XpsPrint API。此 API 在 Windows 7、Windows Server 2008 R2 和 Windows Vista 上可用，前提是安装了 Windows Vista 的平台更新。

Since Aspose.Diagram can easily convert any document to XPS, we only need to write code that passes an XPS document to the XpsPrint API. The only problem is that the XpsPrint API is unmanaged and it requires some knowledge of the Platform Invoke.
### **编码**
我们已经使用 Print 方法创建了 XpsPrintHelper 类，它非常易于使用。您只需指定要打印的文档、打印机名称和可选的作业名称。如果提交或打印文档有任何问题，该方法将抛出异常。

最后一个参数是一个布尔值，它指定代码是应该等到作业被打印出来，还是在提交打印作业后立即返回。如果选择立即返回，则最终无法判断文档是否打印成功。
#### **编程范例**
The following code example shows how to invoke the utility class to print via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


There are two overloads of the XpsPrintHelper.Print method. The first overload takes an Aspose.Diagram.Diagram object and saves it into a MemoryStream in the XPS format. Then it invokes the other XpsPrintHelper.Print overload.

If you want to use this sample without Aspose.Diagram (e.g. you already have an XPS document and just want to print it from an ASP.NET or Windows Service application), then you can just delete this method.
#### **XPS Stream and Print Programming Sample**
This code example convert a Diagram into an XPS stream and print.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


The second XpsPrintHelper.Print overload accepts a Stream object. The stream must contain a document in the XPS format. This method starts an XPS print job, sends the document to the XpsPrint API and then waits for the result if needed.
#### **XpsPrint API 编程示例**
This code example prints an XPS document using the XpsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


StartJob、CopyJob、WaitForJob 和 CheckJobStatus 方法的代码以及 IXpsPrintJob 和 IXpsPrintJobStream 接口的定义都非常低级，并使用 Platform Invoke 和 COM Interop。为简洁起见，此代码未包含在本文中，但可以在示例下载中找到。

XpsPrint API 还提供了额外的功能，例如监控作业进度，但我们的 XpsPrintHelper 是一个非常简单的包装器，不会公开此功能。如果你愿意，你可以自己添加这个。

{{% alert color="primary" %}}

当您运行该项目时，它会在指定的打印机上打印一个示例文档。为了使结果可见，控制台窗口打开。如果抛出异常，程序会显示成功消息或异常文本。

{{% /alert %}}
## **打印 Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)提供四种用于打印图表的重载方法。这些方法足够灵活，可以将 diagram 打印到默认打印机或任何具有自定义设置的可用打印机。您只需要根据需要选择合适的打印方式即可。
### **打印到默认打印机**
在 Aspose.Diagram for .NET 中将 diagram 打印到默认打印机非常简单。执行以下步骤以将 diagram 打印到默认打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 调用 Diagram 对象公开的不带参数的 Print 方法
#### **打印到默认打印机编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **打印到特定打印机**
将 diagram 打印到特定打印机需要打印机的名称作为 Diagram 的打印方法的参数。执行以下步骤以将 diagram 打印到所需的打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 以打印机名称作为字符串参数调用Diagram类的Print方法给Print方法
#### **打印到特定打印机编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **设置打印机和文档名称**
Aspose.Diagram API 允许为打印作业设置特定的打印机和文档名称。执行以下步骤以将 diagram 打印到所需的打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 以打印机和文档名称作为字符串参数调用Diagram类的Print方法给Print方法
#### **设置打印机和文档名称编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}
