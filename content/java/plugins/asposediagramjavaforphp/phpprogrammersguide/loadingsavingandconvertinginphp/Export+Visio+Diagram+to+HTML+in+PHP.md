+++
title = "Export Visio Diagram to HTML in PHP" 
description = "" 
weight = 20173 
+++

Aspose.Diagram for Java : Export Visio Diagram to HTML in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to HTML in PHP


## Aspose.Diagram - Export Visio Diagram to HTML

To Export Visio Diagram to HTML using **Aspose.Diagram Java for PHP**, simply invoke **ExportToHtml** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Save as Html
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to HTML (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)

