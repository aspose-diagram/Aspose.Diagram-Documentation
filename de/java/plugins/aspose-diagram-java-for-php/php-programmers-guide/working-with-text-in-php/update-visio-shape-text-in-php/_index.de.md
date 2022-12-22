---
title: Update Visio Formtext in PHP
type: docs
weight: 30
url: /de/java/update-visio-shape-text-in-php/
---
## **Aspose.Diagram – Update Visio Formtext**
So aktualisieren Sie Visio Shape Text mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ShapeText aktualisieren** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {

$shape->getText()->getValue()->clear();

$shape->getText()->getValue()->add(new Txt("New Text"));

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);

print "Updated shape text.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Formtext aktualisieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
