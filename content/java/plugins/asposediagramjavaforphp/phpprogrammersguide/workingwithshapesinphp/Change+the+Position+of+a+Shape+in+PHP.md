+++
title = "Change the Position of a Shape in PHP" 
description = "" 
weight = 20210 
+++

Aspose.Diagram for Java : Change the Position of a Shape in PHP  

# Aspose.Diagram for Java : Change the Position of a Shape in PHP


## Aspose.Diagram - Change the Position of a Shape

To Change the Position of a Shape using **Aspose.Diagram Java for PHP**, simply invoke **ChangeShapePosition** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();
$i = 0;
while ($i<(int)(string)$shapes->getCount()) {
$shape = $shapes->get($i);
if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 2) {
$shape->move(1, 1);
}
$i += 1;
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."ChangeShapePosition.vdx",$saveFileFormat->VDX);
print"Changed postion of a shape.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Change the Position of a Shape (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)

