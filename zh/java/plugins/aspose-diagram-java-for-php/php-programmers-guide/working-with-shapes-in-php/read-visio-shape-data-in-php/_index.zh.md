---
title: 在 PHP 中读取 Visio 形状数据
type: docs
weight: 50
url: /zh/java/read-visio-shape-data-in-php/
---
## **Aspose.Diagram - 读取所有形状属性**
使用读取所有形状属性**Aspose.Diagram Java 用于 PHP**， 称呼**读取所有形状属性**的方法**读取形状数据**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **Aspose.Diagram - 按名称读取形状属性**
要按名称读取形状属性，请使用**Aspose.Diagram Java 用于 PHP**， 称呼**按名称读取形状属性**的方法**读取形状数据**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **下载运行代码**
下载**读取 Visio 形状数据 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReadShapeData.php)
