+++
title = "Protect and Unprotect a Visio Shape in PHP" 
description = "" 
weight = 20207 
+++

Aspose.Diagram for Java : Protect and Unprotect a Visio Shape in PHP  

# Aspose.Diagram for Java : Protect and Unprotect a Visio Shape in PHP


## Aspose.Diagram - Protect and Unprotect a Visio Shape

To Protect and Unprotect a Visio Shape using **Aspose.Diagram Java for PHP**, simply invoke **ProtectUnprotectShape** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
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

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir . "ProtectUnprotectShape.vdx", $saveFileFormat->VDX);

print "Applied protection on shape successfully!".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Protect and Unprotect a Visio Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectShape.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithProtection/ProtectUnprotectShape.php)

