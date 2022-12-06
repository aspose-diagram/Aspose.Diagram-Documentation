---
title: 在 PHP 中将 Visio Diagram 导出为 PDF
type: docs
weight: 40
url: /zh/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - 将 Visio Diagram 导出为 PDF**
将 Visio Diagram 导出为 PDF 使用**Aspose.Diagram Java 用于 PHP** 只需调用**导出为PDF**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出为 PDF (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
