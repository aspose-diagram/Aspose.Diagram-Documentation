+++
title = "Export Visio Diagram to PDF in PHP" 
description = "" 
weight = 20175 
+++

Aspose.Diagram for Java : Export Visio Diagram to PDF in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to PDF in PHP


## Aspose.Diagram - Export Visio Diagram to PDF

To Export Visio Diagram to PDF using **Aspose.Diagram Java for PHP**, simply invoke **ExportToPdf** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."drawing.vsd");

# Save as PDF file format
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);
print "Exported visio diagram to pdf.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to PDF (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)

