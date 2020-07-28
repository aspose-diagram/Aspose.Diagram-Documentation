+++
title = "Retrieve Drawing Font Information in PHP" 
description = "" 
weight = 20190 
+++

Aspose.Diagram for Java : Retrieve Drawing Font Information in PHP  

# Aspose.Diagram for Java : Retrieve Drawing Font Information in PHP


## Aspose.Diagram - Retrieve Drawing Font Information

To Retrieve Drawing Font Information using **Aspose.Diagram Java for PHP**, simply invoke **GetDiagramFontInfo** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Create instance of Diagram
$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;
while ($i<sizeof($fonts->getCount())) {
$font = $fonts->get($i);
# Display information about the fonts
print $font->getName();
$i+=1;
}
{{< /code >}}

## Download Running Code

Download **Retrieve Drawing Font Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)

