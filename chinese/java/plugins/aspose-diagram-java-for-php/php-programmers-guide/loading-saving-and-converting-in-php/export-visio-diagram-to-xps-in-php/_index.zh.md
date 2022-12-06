---
title: Export Visio Diagram to XPS in PHP
type: docs
weight: 80
url: /zh/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java 用于 PHP** 只需调用**导出到 Xps**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**Export Visio Diagram to XPS (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
