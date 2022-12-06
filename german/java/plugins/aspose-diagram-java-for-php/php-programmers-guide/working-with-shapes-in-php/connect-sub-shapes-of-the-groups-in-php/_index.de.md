---
title: Verbinden Sie Unterformen der Gruppen in PHP
type: docs
weight: 20
url: /de/java/connect-sub-shapes-of-the-groups-in-php/
---
## **Aspose.Diagram - Unterformen der Gruppen verbinden**
 Um Unterformen der Gruppen zu verbinden, verwenden Sie**Aspose.Diagram Java für PHP** , einfach aufrufen**ConnectSubShapes** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# Access a particular page

$page = $diagram->getPages()->getPage("Flow 1");

\# Set sub shape ids

$shape_from_id = 1;

$shape_to_id = 9;

\# Initialize connector shape

$shape=new Shape();

$shape->getLine()->getEndArrow()->setValue(5);

$shape->getLine()->getLineWeight()->setValue(0.01388);

\# Add shape

$connecter_id=$diagram->addShape($shape,"Dynamic connector",$page->getID());

\# Connect sub-shapes

$connection_point_place = new ConnectionPointPlace();

$page->connectShapesViaConnector($shape_from_id,$connection_point_place->RIGHT,$shape_to_id,$connection_point_place->LEFT,$connecter_id);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ConnectSubShapes.vdx",$saveFileFormat->VDX);

print "Connected sub-shapes of a group.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Unterformen der Gruppen verbinden (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ConnectSubShapes.php)
