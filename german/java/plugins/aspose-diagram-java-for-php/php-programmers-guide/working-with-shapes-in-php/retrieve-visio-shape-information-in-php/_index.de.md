---
title: Rufen Sie Visio Shape-Informationen in PHP ab
type: docs
weight: 70
url: /de/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - Abrufen von Visio-Shape-Informationen**
 Abrufen von Visio-Shape-Informationen mit**Aspose.Diagram Java für PHP** , einfach aufrufen**GetShapeInfo** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Forminformationen abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
