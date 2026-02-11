---
title: 使用打印
type: docs
weight: 80
url: /zh/java/working-with-print/
---
## **打印 Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)提供四种用于打印图表的重载方法。这些方法足够灵活，可以将 diagram 打印到默认打印机或任何具有自定义设置的可用打印机。您只需要根据需要选择合适的打印方式即可。
### **打印到特定打印机**
将 diagram 打印到特定打印机需要打印机的名称作为 Diagram 的打印方法的参数。执行以下步骤以将 diagram 打印到所需的打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 以打印机名称作为字符串参数调用Diagram类的Print方法给Print方法
#### **打印到特定打印机编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **设置打印机和文档名称**
Aspose.Diagram API 允许为打印作业设置特定的打印机和文档名称。执行以下步骤以将 diagram 打印到所需的打印机：

- 创建 Diagram 类的实例以加载要打印的 diagram
- 以打印机和文档名称作为字符串参数调用Diagram类的Print方法给Print方法
#### **设置打印机和文档名称编程示例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

