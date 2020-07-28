+++
title = "Read Visio Shape Data in PHP" 
description = "" 
weight = 20214 
+++

Aspose.Diagram for Java : Read Visio Shape Data in PHP  

# Aspose.Diagram for Java : Read Visio Shape Data in PHP


## Aspose.Diagram - Read All Shape Properties

To Read All Shape Properties using **Aspose.Diagram Java for PHP**, call **read\_all\_shape\_properties** method of **ReadShapeData** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
public static function read_all_shape_properties($dataDir=null)
{

# Create instance of Diagram
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
{{< /code >}}

## Aspose.Diagram - Read a Shape Property by Name

To Read a Shape Property by Name using **Aspose.Diagram Java for PHP**, call **read\_shape\_property\_by\_name** method of **ReadShapeData** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
public static function read_shape_property_by_name($dataDir=null){

# Create instance of Diagram
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
{{< /code >}}

## Download Running Code

Download **Read Visio Shape Data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)

