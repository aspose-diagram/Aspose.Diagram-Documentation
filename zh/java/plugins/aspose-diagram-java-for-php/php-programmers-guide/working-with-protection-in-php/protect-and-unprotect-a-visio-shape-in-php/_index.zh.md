---
title: 在 PHP 中保护和取消保护 Visio 形状
type: docs
weight: 10
url: /zh/java/protect-and-unprotect-a-visio-shape-in-php/
---
## **Aspose.Diagram - 保护和取消保护 Visio 形状**
要保护和取消保护 Visio 形状，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**保护取消保护形状**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."drawing.vsd");

$page=$diagram->getPages()->getPage("Flow 1");

$shape=$page->getShapes()->getShape(1);

$shape->getProtection()->getLockAspect()->setValue(1);

$shape->getProtection()->getLockBegin()->setValue(1);

$shape->getProtection()->getLockCalcWH()->setValue(1);

$shape->getProtection()->getLockCrop()->setValue(1);

$shape->getProtection()->getLockCustProp()->setValue(1);

$shape->getProtection()->getLockDelete()->setValue(1);

$shape->getProtection()->getLockEnd()->setValue(1);

$shape->getProtection()->getLockFormat()->setValue(1);

$shape->getProtection()->getLockFromGroupFormat()->setValue(1);

$shape->getProtection()->getLockGroup()->setValue(1);

$shape->getProtection()->getLockHeight()->setValue(1);

$shape->getProtection()->getLockMoveX()->setValue(1);

$shape->getProtection()->getLockMoveY()->setValue(1);

$shape->getProtection()->getLockRotate()->setValue(1);

$shape->getProtection()->getLockSelect()->setValue(1);

$shape->getProtection()->getLockTextEdit()->setValue(1);

$shape->getProtection()->getLockThemeColors()->setValue(1);

$shape->getProtection()->getLockThemeEffects()->setValue(1);

$shape->getProtection()->getLockVtxEdit()->setValue(1);

$shape->getProtection()->getLockWidth()->setValue(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectShape.vdx", $saveFileFormat->VDX);

print "Applied protection on shape successfully!".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**保护和取消保护 Visio 形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectShape.php)
