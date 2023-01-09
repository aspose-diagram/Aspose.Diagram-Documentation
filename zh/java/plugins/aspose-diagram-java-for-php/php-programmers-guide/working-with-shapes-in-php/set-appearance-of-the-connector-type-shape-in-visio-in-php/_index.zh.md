---
title: 在 Visio 中用 PHP 设置连接器类型形状的外观
type: docs
weight: 100
url: /zh/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram - 在 Visio 中设置连接器类型形状的外观**
要在 Visio 中设置连接器类型形状的外观，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**设置形状外观**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set dynamic connector appearance

$connectorsTypeValue=new ConnectorsTypeValue();

$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);

print "Set appearnce of the connector type shape.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**Visio（Aspose.Diagram）中设置连接器类型形状的外观**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
