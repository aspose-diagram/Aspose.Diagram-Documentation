---
title: 在 PHP 中将 Visio Diagram 导出到 XAML
type: docs
weight: 60
url: /zh/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - 将 Visio Diagram 导出到 XAML**
将 Visio Diagram 导出到 XAML 使用**Aspose.Diagram Java 用于 PHP** 只需调用**导出到 Xaml**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出到 XAML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
