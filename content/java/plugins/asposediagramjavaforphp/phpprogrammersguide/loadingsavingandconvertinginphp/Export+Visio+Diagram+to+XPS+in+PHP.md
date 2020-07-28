+++
title = "Export Visio Diagram to XPS in PHP" 
description = "" 
weight = 20179 
+++

Aspose.Diagram for Java : Export Visio Diagram to XPS in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to XPS in PHP


## Aspose.Diagram - Export Visio Diagram to XPS

To Export Visio Diagram to XPS using **Aspose.Diagram Java for PHP**, simply invoke **ExportToXps** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Save as XPS
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to XPS (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)

