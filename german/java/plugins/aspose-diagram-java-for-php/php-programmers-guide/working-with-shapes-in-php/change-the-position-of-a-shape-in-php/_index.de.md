---
title: Ändern Sie die Position einer Form in PHP
type: docs
weight: 10
url: /de/java/change-the-position-of-a-shape-in-php/
---
## **Aspose.Diagram - Ändern Sie die Position einer Form**
 So ändern Sie die Position einer Form mit**Aspose.Diagram Java für PHP** , einfach aufrufen**FormPosition ändern** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Ändern der Position einer Form (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
