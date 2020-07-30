---
title : "Set Milestone Shape Properties in PHP" 
description : "" 
weight : 20220 
toc : false
type: docs
url: /java/plugins/php/guide/shapes/set+milestone+shape+properties+in+php/
---

# Aspose.Diagram for Java : Set Milestone Shape Properties in PHP


## Aspose.Diagram - Set Milestone Shape Properties

To Set Milestone Shape Properties using **Aspose.Diagram Java for PHP**, simply invoke **SetMilestoneShapeProperties** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."Drawing.vsd");

$shape_id=1;

# Get timeline shape
$milestone=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape($shape_id);

# Initialize MilestoneHelper object
$milestone_helper = new MilestoneHelper($milestone);

# Set date format
$milestone_helper->setDateFormat(21);

# Set auto update flag
$milestone_helper->setAutoUpdate(true);

# Set milestone type
$milestone_helper->setType(6);

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."SetMilestoneShapeProperties.vdx", $saveFileFormat->VDX);
print "Set milestone shape properties.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Set Milestone Shape Properties (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/SetMilestoneShapeProperties.php)

