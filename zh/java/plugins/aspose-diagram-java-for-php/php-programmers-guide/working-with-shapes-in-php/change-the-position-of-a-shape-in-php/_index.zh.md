---
title: 在 PHP 中更改形状的位置
type: docs
weight: 10
url: /zh/java/change-the-position-of-a-shape-in-php/
---
## **Aspose.Diagram - 更改形状的位置**
要使用更改形状的位置**Aspose.Diagram Java 用于 PHP** 只需调用**改变形状位置**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 2) {

$shape->move(1, 1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ChangeShapePosition.vdx",$saveFileFormat->VDX);

print"Changed postion of a shape.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**更改形状的位置 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
