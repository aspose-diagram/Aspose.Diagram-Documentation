---
title : "Update Visio Shape Text in PHP" 
description : "" 
weight : 20231 
toc : false
type: docs
url: /java/plugins/php/guide/text/update+visio+shape+text+in+php/
---

# Aspose.Diagram for Java : Update Visio Shape Text in PHP


## Aspose.Diagram - Update Visio Shape Text

To Update Visio Shape Text using **Aspose.Diagram Java for PHP**, simply invoke **UpdateShapeText** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();
$i=0;
while($i<(int)(string)$shapes->getCount()) {
$shape = $shapes->get($i);
if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {
$shape->getText()->getValue()->clear();
$shape->getText()->getValue()->add(new Txt("New Text"));
}
$i += 1;
}

# Save diagram
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);
print "Updated shape text.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Update Visio Shape Text (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithText/UpdateShapeText.php)

