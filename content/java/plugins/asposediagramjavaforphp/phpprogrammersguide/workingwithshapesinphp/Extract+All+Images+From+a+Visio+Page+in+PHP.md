+++
title = "Extract All Images From a Visio Page in PHP" 
description = "" 
weight = 20212 
+++

Aspose.Diagram for Java : Extract All Images From a Visio Page in PHP  

# Aspose.Diagram for Java : Extract All Images From a Visio Page in PHP


## Aspose.Diagram - Extract All Images From a Visio Page

To Extract All Images From a Visio Page using **Aspose.Diagram Java for PHP**, simply invoke **ExtractImages** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();
$i = 0;
$typeValue=new TypeValue();
while ($i <(int)(string)$shapes->getCount()){
$shape = $shapes->get($i);
# Filter shapes by type Foreign
if ($shape->getType()== $typeValue->FOREIGN){
# create an image file
$fos = new FileOutputStream($dataDir."Image#{i}.bmp");
$fos->write($shape->getForeignData()->getValue());
$fos->close();
}
$i += 1;
}
print "Extracted images successfully!".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Extract All Images From a Visio Page (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithShapes/ExtractImages.php)

