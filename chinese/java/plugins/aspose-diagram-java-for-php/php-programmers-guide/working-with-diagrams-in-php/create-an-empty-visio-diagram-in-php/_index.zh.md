---
title: 在 PHP 中创建一个空的 Visio Diagram
type: docs
weight: 20
url: /zh/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - 创建一个空的 Visio Diagram**
创建一个空的 Visio Diagram 使用**Aspose.Diagram Java 用于 PHP** 只需调用**创建图表**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**创建一个空的 Visio Diagram (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
