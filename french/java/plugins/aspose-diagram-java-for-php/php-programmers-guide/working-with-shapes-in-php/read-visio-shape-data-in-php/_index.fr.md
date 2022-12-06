---
title: Lire les données de forme Visio en PHP
type: docs
weight: 50
url: /fr/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram - Lire toutes les propriétés de forme**
 Pour lire toutes les propriétés de forme à l'aide**Aspose.Diagram Java pour PHP** , appel**read_all_shape_properties** méthode de**LireShapeData** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Aspose.Diagram - Lire une propriété de forme par nom**
 Pour lire une propriété de forme par nom à l'aide**Aspose.Diagram Java pour PHP** , appel**read_shape_property_by_name** méthode de**LireShapeData** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Lire les données de forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
