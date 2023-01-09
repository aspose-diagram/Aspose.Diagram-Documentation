---
title: 在 PHP 中设置 Visio Shape 的 XForm 数据
type: docs
weight: 150
url: /zh/java/set-visio-shape-s-xform-data-in-php/
---
## **Aspose.Diagram - 设置 Visio Shape 的 XForm 数据**
设置 Visio Shape 的 XForm 数据使用**Aspose.Diagram Java 用于 PHP** 只需调用**设置形状XFormData**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

if ($shape->getNameU()=="process" && $shape->getID() == 1) {

$shape->getXForm()->getPinX()->setValue(5);

$shape->getXForm()->getPinY()->setValue(5);

}

$i+= 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeXFormData.vdx",$saveFileFormat->VDX);

print "Set visio shape's XForm data.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**设置 Visio Shape 的 XForm 数据 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
