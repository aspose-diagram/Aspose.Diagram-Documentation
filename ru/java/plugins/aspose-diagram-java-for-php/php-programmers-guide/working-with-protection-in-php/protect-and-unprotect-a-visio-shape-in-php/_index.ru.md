---
title: Защита и снятие защиты формы Visio в PHP
type: docs
weight: 10
url: /ru/java/protect-and-unprotect-a-visio-shape-in-php/
---
## **Aspose.Diagram - Защита и снятие защиты формы Visio**
 Чтобы защитить и снять защиту формы Visio, используя**Aspose.Diagram Java для PHP** , просто вызовите**ProtectUnprotectShape** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Защита и снятие защиты формы Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectShape.php)
