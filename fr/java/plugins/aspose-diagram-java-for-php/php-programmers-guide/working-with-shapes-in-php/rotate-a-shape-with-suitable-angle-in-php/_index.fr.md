---
title: Faire pivoter une forme avec un angle approprié en PHP
type: docs
weight: 80
url: /fr/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Faire pivoter une forme avec un angle approprié**
 Pour faire pivoter une forme avec un angle approprié à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**RotationForme** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Faire pivoter une forme avec un angle approprié (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
