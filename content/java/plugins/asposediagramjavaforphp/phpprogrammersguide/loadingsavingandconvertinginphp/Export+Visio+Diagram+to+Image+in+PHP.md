+++
title = "Export Visio Diagram to Image in PHP" 
description = "" 
weight = 20174 
+++

Aspose.Diagram for Java : Export Visio Diagram to Image in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to Image in PHP


## Aspose.Diagram - Export Visio Diagram to Image

To Export Visio Diagram to Image using **Aspose.Diagram Java for PHP**, simply invoke **ExportToImage** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Save as PNG
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to Image (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)

