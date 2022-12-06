---
title: 在 PHP 中设置形状的高度和宽度
type: docs
weight: 120
url: /zh/java/set-the-height-and-width-of-a-shape-in-php/
---
## **Aspose.Diagram - 设置形状的高度和宽度**
设置形状的高度和宽度使用**Aspose.Diagram Java 用于 PHP** 只需调用**设置形状高度和宽度**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i <sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ((string)$shape->getNameU()=="Process" && (int)(string)$shape->getID()==1) {

$shape->setWidth(2 * (int)(string)$shape->getXForm()->getWidth()->getValue());

$shape->setHeight(2 * (int)(string)$shape->getXForm()->getHeight()->getValue());

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeHeightAndWidth.vdx",$saveFileFormat->VDX);

print "Set height and width of shape.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**设置形状的高度和宽度 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeHeightAndWidth.php)
