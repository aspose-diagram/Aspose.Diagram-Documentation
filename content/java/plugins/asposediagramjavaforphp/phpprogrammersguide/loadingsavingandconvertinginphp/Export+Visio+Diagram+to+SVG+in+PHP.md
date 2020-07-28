+++
title = "Export Visio Diagram to SVG in PHP" 
description = "" 
weight = 20176 
+++

Aspose.Diagram for Java : Export Visio Diagram to SVG in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to SVG in PHP


## Aspose.Diagram - Export Visio Diagram to SVG

To Export Visio Diagram to SVG using **Aspose.Diagram Java for PHP**, simply invoke **ExportToSvg** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Save as SVG
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to SVG (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)

