---
title: Drehen Sie eine Form mit einem geeigneten Winkel in PHP
type: docs
weight: 80
url: /de/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Drehen Sie eine Form mit einem geeigneten Winkel**
 So drehen Sie eine Form mit einem geeigneten Winkel**Aspose.Diagram Java für PHP** , einfach aufrufen**RotateShape** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Drehen einer Form mit geeignetem Winkel (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
