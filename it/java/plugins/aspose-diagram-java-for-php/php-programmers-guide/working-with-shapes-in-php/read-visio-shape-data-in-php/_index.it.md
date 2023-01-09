---
title: Leggi Visio Shape Data in PHP
type: docs
weight: 50
url: /it/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram - Leggi tutte le proprietà della forma**
 Per leggere tutte le proprietà della forma utilizzando**Aspose.Diagram Java per PHP** , chiamata**read_all_shape_properties** metodo di**ReadShapeData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Aspose.Diagram - Leggere una proprietà Shape per nome**
 Per leggere una proprietà Shape per nome utilizzando**Aspose.Diagram Java per PHP** , chiamata**read_shape_property_by_name** metodo di**ReadShapeData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Leggi Visio Dati forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
