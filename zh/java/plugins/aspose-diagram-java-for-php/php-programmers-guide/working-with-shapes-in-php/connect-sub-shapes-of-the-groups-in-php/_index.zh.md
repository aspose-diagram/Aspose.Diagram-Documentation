---
title: 在 PHP 中连接组的子形状
type: docs
weight: 20
url: /zh/java/connect-sub-shapes-of-the-groups-in-php/
---
## **Aspose.Diagram - 连接组的子形状**
使用以下方法连接组的子形状**Aspose.Diagram Java 用于 PHP** 只需调用**连接子形状**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# Access a particular page

$page = $diagram->getPages()->getPage("Flow 1");

\# Set sub shape ids

$shape_from_id = 1;

$shape_to_id = 9;

\# Initialize connector shape

$shape=new Shape();

$shape->getLine()->getEndArrow()->setValue(5);

$shape->getLine()->getLineWeight()->setValue(0.01388);

\# Add shape

$connecter_id=$diagram->addShape($shape,"Dynamic connector",$page->getID());

\# Connect sub-shapes

$connection_point_place = new ConnectionPointPlace();

$page->connectShapesViaConnector($shape_from_id,$connection_point_place->RIGHT,$shape_to_id,$connection_point_place->LEFT,$connecter_id);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ConnectSubShapes.vdx",$saveFileFormat->VDX);

print "Connected sub-shapes of a group.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**连接组的子形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ConnectSubShapes.php)
