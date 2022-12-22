---
title: Leer Visio datos de forma en PHP
type: docs
weight: 50
url: /es/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram - Leer todas las propiedades de forma**
 Para leer todas las propiedades de forma usando**Aspose.Diagram Java para PHP** , llamar**read_all_shape_properties** método de**LeerFormaDatos** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Aspose.Diagram - Leer una propiedad de forma por nombre**
 Para leer una propiedad de forma por nombre usando**Aspose.Diagram Java para PHP** , llamar**leer_forma_propiedad_por_nombre** método de**LeerFormaDatos** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Leer Visio Datos de forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
