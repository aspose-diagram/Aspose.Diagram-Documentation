---
title: Lesen Sie Visio Formdaten in PHP
type: docs
weight: 50
url: /de/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram – Alle Shape-Eigenschaften lesen**
 So lesen Sie alle Formeigenschaften mit**Aspose.Diagram Java für PHP** , Anruf**read_all_shape_properties** Methode von**ReadShapeData** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 public static function read_all_shape_properties($dataDir=null)

{

\# Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i <(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

if ($shape->getName() == "Process") {

$j = 0;

while ($j<(int)(string)$shape->getProps()->getCount()) {

$property = $shape->getProps()->get($j);

print $property->getLabel()->getValue() . ": " . $property->getValue()->getVal();

$j += 1;

}

break;

}

$i += 1;

}

}

{{< /highlight >}}
## **Aspose.Diagram – Lesen Sie eine Shape-Eigenschaft nach Namen**
 So lesen Sie eine Formeigenschaft nach Namen mit**Aspose.Diagram Java für PHP** , Anruf**read_shape_property_by_name** Methode von**ReadShapeData** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 public static function read_shape_property_by_name($dataDir=null){

\# Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getName() == "Process") {

$property=$shape->getProps()->getProp("Cost");

print $property->getLabel()->getValue().": ".$property->getValue()->getVal().PHP_EOL;

}

$i+= 1;

}

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Formdaten lesen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
