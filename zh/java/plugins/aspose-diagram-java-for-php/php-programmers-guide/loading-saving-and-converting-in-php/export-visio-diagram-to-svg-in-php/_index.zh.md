---
title: Export Visio Diagram to SVG in PHP
type: docs
weight: 50
url: /zh/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java 用于 PHP** 只需调用**导出到 Svg**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**Export Visio Diagram to SVG (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
