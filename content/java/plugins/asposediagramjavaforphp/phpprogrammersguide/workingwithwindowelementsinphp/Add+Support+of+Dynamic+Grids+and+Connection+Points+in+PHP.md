+++
title = "Add Support of Dynamic Grids and Connection Points in PHP" 
description = "" 
weight = 20237 
+++

Aspose.Diagram for Java : Add Support of Dynamic Grids and Connection Points in PHP  

# Aspose.Diagram for Java : Add Support of Dynamic Grids and Connection Points in PHP


## Aspose.Diagram - Add Support of Dynamic Grids and Connection Points

To Add Support of Dynamic Grids and Connection Points using **Aspose.Diagram Java for PHP**, simply invoke **AddDynamicGridsAndConnectionPoints** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

# get window object by index
$window=$diagram->getWindows()->get(0);

# check dynamic grid option
$window->setDynamicGridEnabled(1);

# check connection points option
$window->setShowConnectionPoints(1);

# Save as VDX
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Add Support of Dynamic Grids and Connection Points (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)

