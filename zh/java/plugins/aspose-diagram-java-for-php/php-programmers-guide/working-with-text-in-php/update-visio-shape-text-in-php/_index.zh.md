---
title: 更新 Visio PHP 中的形状文本
type: docs
weight: 30
url: /zh/java/update-visio-shape-text-in-php/
---
## **Aspose.Diagram - 更新 Visio 形状文本**
使用更新 Visio 形状文本**Aspose.Diagram Java 用于 PHP** 只需调用**更新形状文本**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {

$shape->getText()->getValue()->clear();

$shape->getText()->getValue()->add(new Txt("New Text"));

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);

print "Updated shape text.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**更新 Visio 形状文本 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
