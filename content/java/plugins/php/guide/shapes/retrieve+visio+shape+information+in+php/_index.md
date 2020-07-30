---
title : "Retrieve Visio Shape Information in PHP" 
description : "" 
weight : 20216 
toc : false
type: docs
url: /java/plugins/php/guide/shapes/retrieve+visio+shape+information+in+php/
---

# Aspose.Diagram for Java : Retrieve Visio Shape Information in PHP


## Aspose.Diagram - Retrieve Visio Shape Information

To Retrieve Visio Shape Information using **Aspose.Diagram Java for PHP**, simply invoke **GetShapeInfo** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;
while ($i<(int)(string)$shapes->getCount()) {
$shape = $shapes->get($i);
# Display information about the shapes
print "Shape ID : " . (string)$shape->getID().PHP_EOL;
print "Name : " . (string)$shape->getName().PHP_EOL;
print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;
$i += 1;
}
{{< /code >}}

## Download Running Code

Download **Retrieve Visio Shape Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)

