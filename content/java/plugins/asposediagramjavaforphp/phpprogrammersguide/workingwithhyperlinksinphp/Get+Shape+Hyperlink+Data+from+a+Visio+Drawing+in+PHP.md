+++
title = "Get Shape Hyperlink Data from a Visio Drawing in PHP" 
description = "" 
weight = 20198 
+++

Aspose.Diagram for Java : Get Shape Hyperlink Data from a Visio Drawing in PHP  

# Aspose.Diagram for Java : Get Shape Hyperlink Data from a Visio Drawing in PHP


## Aspose.Diagram - Get Shape Hyperlink Data

To Get Shape Hyperlink Data using **Aspose.Diagram Java for PHP**, simply invoke **GetShapeHyperlinkData** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir . "drawing.vdx");

# Get a particular shape
$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

$hyperlinks=$shape->getHyperlinks();

$i=0;
while ($i<(int)(string)$hyperlinks->getCount()) {
$hyperlink=$hyperlinks->get($i);
print "Address: " . (string)$hyperlink->getAddress()->getValue();
print "Sub Address: " . (string)$hyperlink->getSubAddress()->getValue();
print "Description: " . (string)$hyperlink->getDescription()->getValue();
$i+=1;
}
{{< /code >}}

## Download Running Code

Download **Get Shape Hyperlink Data from a Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)

