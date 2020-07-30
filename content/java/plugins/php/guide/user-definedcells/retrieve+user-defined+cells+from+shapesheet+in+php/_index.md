---
title : "Retrieve User-defined Cells from Shapesheet in PHP" 
description : "" 
weight : 20235 
toc : false
type: docs
url: /java/plugins/php/guide/user-definedcells/retrieve+user-defined+cells+from+shapesheet+in+php/
---

# Aspose.Diagram for Java : Retrieve User-defined Cells from Shapesheet in PHP


## Aspose.Diagram - Retrieve User-defined Cells from Shapesheet

To Retrieve User-defined Cells from Shapesheet using **Aspose.Diagram Java for PHP**, simply invoke **GetUserDefinedCells** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram=new Diagram($dataDir . "drawing.vdx");

$pages=$diagram->getPages();

$count=0;
while($count<(int)(string)$pages->getCount()) {
$page = $pages->get($count);
$shapes = $page->getShapes();
$i = 0;
while ($i<(int)(string)$shapes->getCount()) {
$shape = $shapes->get($i);
if ($shape->getNameU() == "Process") {
$users = $shape->getUsers();
$j = 0;
while ($j<(int)(string)$users->getCount()) {
$user = $users->get($j);
print "Name: " . $user->getNameU() . " Value: " . $user->getValue()->getVal() . " Prompt: " . $user->getPrompt()->getValue();
$j += 1;
}
break;
}
$i += 1;
}
$count += 1;
}
{{< /code >}}

## Download Running Code

Download **Retrieve User-defined Cells from Shapesheet (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)

