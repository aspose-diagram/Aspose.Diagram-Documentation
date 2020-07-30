---
title : "Set Visio Shapes XForm Data in PHP" 
description : "" 
weight : 20224 
toc : false
type: docs
url: /java/plugins/php/guide/shapes/set+visio+shapes+xform+data+in+php/
---

# Aspose.Diagram for Java : Set Visio Shape's XForm Data in PHP


## Aspose.Diagram - Set Visio Shape's XForm Data

To Set Visio Shape's XForm Data using **Aspose.Diagram Java for PHP**, simply invoke **SetShapeXFormData** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;
while ($i<(int)(string)$shapes->getCount()){
$shape = $shapes->get($i);
if ($shape->getNameU()=="process" && $shape->getID() == 1) {
$shape->getXForm()->getPinX()->setValue(5);
$shape->getXForm()->getPinY()->setValue(5);
}
$i+= 1;
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."SetShapeXFormData.vdx",$saveFileFormat->VDX);
print "Set visio shape's XForm data.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Set Visio Shape's XForm Data (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)

