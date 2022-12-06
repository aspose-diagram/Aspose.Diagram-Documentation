---
title: 将 Visio Diagram 导出为 PHP 中的图像
type: docs
weight: 30
url: /zh/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - 导出 Visio Diagram 到图像**
将 Visio Diagram 导出到图像使用**Aspose.Diagram Java 用于 PHP** 只需调用**导出到图像**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出到图像 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
