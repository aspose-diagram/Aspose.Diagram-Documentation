---
title: Proteger y desproteger una forma Visio en PHP
type: docs
weight: 10
url: /es/java/protect-and-unprotect-a-visio-shape-in-php/
---
## **Aspose.Diagram - Proteger y desproteger una forma Visio**
 Para proteger y desproteger una forma Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**ProtegerDesprotegerForma** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Proteger y desproteger una forma Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectShape.php)
