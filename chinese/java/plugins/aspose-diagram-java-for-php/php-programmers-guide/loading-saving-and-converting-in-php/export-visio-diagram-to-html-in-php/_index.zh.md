---
title: 在 PHP 中将 Visio Diagram 导出到 HTML
type: docs
weight: 20
url: /zh/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - 将 Visio Diagram 导出为 HTML**
将 Visio Diagram 导出到 HTML 使用**Aspose.Diagram Java 用于 PHP** 只需调用**导出到 HTML**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出为 HTML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
