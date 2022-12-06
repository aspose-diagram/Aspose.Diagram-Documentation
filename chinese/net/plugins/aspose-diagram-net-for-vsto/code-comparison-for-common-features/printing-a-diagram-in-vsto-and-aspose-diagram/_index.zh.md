---
title: 在 VSTO 中打印 Diagram 和 Aspose.Diagram
type: docs
weight: 100
url: /zh/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **VSTO**
下面是显示如何打印 diagram 的代码：

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
将 diagram 打印到**默认打印机**在 Aspose.Diagram for .NET 中非常简单。执行以下步骤以将 diagram 打印到默认打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 调用 Diagram 对象公开的不带参数的 Print 方法

将 diagram 打印到**特定打印机**需要打印机的名称作为 Diagram 的打印方法的参数。执行以下步骤以将 diagram 打印到所需的打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 以打印机名称作为字符串参数调用Diagram类的Print方法给Print方法

下面是使用默认和特定打印机的代码：

{{< highlight "cs" >}}

  string FilePath = "demo.vsd";

 //Load the diagram

 Diagram diagram = new Diagram(FilePath);

 //Call the print method to print whole Diagram to the default printer

 diagram.Print();

 //Call the print method to print whole Diagram to the desired printer

 diagram.Print("LaserJet1100");

 PrinterSettings settings = new PrinterSettings();

 settings.PrinterName = "LaserJet1100";

 //Call the print method to print whole Diagram to the desired printer and set document name in print job

 diagram.Print(settings, "Job name while printing with Aspose.Diagram");


{{< /highlight >}}
## **下载示例代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **下载运行代码**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
