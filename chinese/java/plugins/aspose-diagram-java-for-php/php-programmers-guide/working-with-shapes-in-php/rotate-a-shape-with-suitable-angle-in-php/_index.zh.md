---
title: 在 PHP 中以合适的角度旋转形状
type: docs
weight: 80
url: /zh/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - 以合适的角度旋转形状**
使用合适的角度旋转形状**Aspose.Diagram Java 用于 PHP** 只需调用**旋转形状**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**以合适的角度旋转形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
