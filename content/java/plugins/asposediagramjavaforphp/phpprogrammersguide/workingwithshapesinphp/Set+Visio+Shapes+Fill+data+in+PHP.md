+++
title = "Set Visio Shapes Fill data in PHP" 
description = "" 
weight = 20222 
+++

Aspose.Diagram for Java : Set Visio Shape's Fill data in PHP  

# Aspose.Diagram for Java : Set Visio Shape's Fill data in PHP


## Aspose.Diagram - Set Visio Shape's Fill data

To Set Visio Shape's Fill data using **Aspose.Diagram Java for Ruby**, simply invoke **SetShapeFillData** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;
while ($i<sizeof($shapes->getCount())) {
$shape = $shapes->get($i);
if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {
$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());
$shape->getFill()->getFillForegnd()->setValue("#ebf8df");
}
$i += 1;
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);
print "Set visio shape's fill data.".PHP_EOL;
}
{{< /code >}}

## Download Running Code

Download **Set Visio Shape's Fill data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)

