---
title: Legen Sie die XForm-Daten von Visio Shape in PHP fest
type: docs
weight: 150
url: /de/java/set-visio-shape-s-xform-data-in-php/
---
## **Aspose.Diagram – Legen Sie die XForm-Daten von Visio Shape fest**
 So legen Sie die XForm-Daten von Visio Shape fest**Aspose.Diagram Java für PHP** , einfach aufrufen**SetShapeXFormData** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

if ($shape->getNameU()=="process" && $shape->getID() == 1) {

$shape->getXForm()->getPinX()->setValue(5);

$shape->getXForm()->getPinY()->setValue(5);

}

$i+= 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeXFormData.vdx",$saveFileFormat->VDX);

print "Set visio shape's XForm data.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**XForm-Daten von Visio Shape festlegen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
