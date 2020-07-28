+++
title = "Set Appearance of the Connector Type Shape in Visio in PHP" 
description = "" 
weight = 20219 
+++

Aspose.Diagram for Java : Set Appearance of the Connector Type Shape in Visio in PHP  

# Aspose.Diagram for Java : Set Appearance of the Connector Type Shape in Visio in PHP


## Aspose.Diagram - Set Appearance of the Connector Type Shape in Visio

To Set Appearance of the Connector Type Shape in Visio using **Aspose.Diagram Java for PHP**, simply invoke **SetShapeAppearance** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram =new Diagram($dataDir."Drawing.vsd");

# Access a particular page
$page=$diagram->getPages()->getPage("Flow 1");

# get a particular connector shape
$shape=$page->getShapes()->getShape(1);

# set dynamic connector appearance
$connectorsTypeValue=new ConnectorsTypeValue();
$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);
print "Set appearnce of the connector type shape.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Set Appearance of the Connector Type Shape in Visio (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)

