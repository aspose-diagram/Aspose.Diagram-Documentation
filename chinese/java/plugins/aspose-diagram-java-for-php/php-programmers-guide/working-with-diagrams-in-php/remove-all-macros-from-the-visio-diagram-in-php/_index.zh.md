---
title: 在 PHP 中删除 Visio Diagram 中的所有宏
type: docs
weight: 30
url: /zh/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - 从 Visio Diagram 中删除所有宏**
要使用 Visio Diagram 删除所有宏**Aspose.Diagram Java 用于 PHP** 只需调用**从图表中移除所有宏**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio Diagram (Aspose.Diagram) 中删除所有宏**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
