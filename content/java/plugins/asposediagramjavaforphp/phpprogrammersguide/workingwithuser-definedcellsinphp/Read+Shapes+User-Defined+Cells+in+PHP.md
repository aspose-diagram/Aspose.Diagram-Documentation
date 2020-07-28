+++
title = "Read Shapes User-Defined Cells in PHP" 
description = "" 
weight = 20234 
+++

Aspose.Diagram for Java : Read Shape's User-Defined Cells in PHP  

# Aspose.Diagram for Java : Read Shape's User-Defined Cells in PHP


## Aspose.Diagram - Read Shape's User-Defined Cells

To Read Shape's User-Defined Cells using **Aspose.Diagram Java for PHP**, simply invoke **ReadUserDefinedCells** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir . "drawing.vdx");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;
while($i<(int)(string)$shapes->getCount()) {
$shape=$shapes->get($i);
if($shape->getNameU()=="Process") {
$users = $shape->getUsers();
$j = 0;
while ($j<(int)(string)$users->getCount()) {
$user = $users->get($j);
print $user->getName() . ": " . $user->getValue()->getVal();
$j += 1;
}
break;
}
$i+=1;
}
{{< /code >}}

## Download Running Code

Download **Read Shape's User-Defined Cells (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)

