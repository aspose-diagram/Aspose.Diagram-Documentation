---
title: 在 PHP 中保存 Visio 文档
type: docs
weight: 100
url: /zh/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - 保存 Visio 文件**
保存 Visio 文档使用**Aspose.Diagram Java 用于 PHP**，您可以使用以下代码。

**PHP代码**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **下载运行代码**
下载**将 Visio Diagram 导出到 XPS (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
