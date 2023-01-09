---
title: Läs Visio Shape Data i PHP
type: docs
weight: 50
url: /sv/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram - Läs alla formegenskaper**
 För att läsa alla formegenskaper med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**read_all_shape_properties** metod av**ReadShapeData** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Läs en Shape Property efter namn**
 För att läsa en formegenskap efter namn med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**read_shape_property_by_name** metod av**ReadShapeData** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Läs Visio Shape Data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
