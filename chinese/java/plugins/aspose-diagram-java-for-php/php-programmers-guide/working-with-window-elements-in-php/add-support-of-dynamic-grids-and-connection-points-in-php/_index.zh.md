---
title: 在 PHP 中添加对动态网格和连接点的支持
type: docs
weight: 10
url: /zh/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - 添加对动态网格和连接点的支持**
要添加对动态网格和连接点的支持，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**添加动态网格和连接点**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**添加对动态网格和连接点的支持 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
