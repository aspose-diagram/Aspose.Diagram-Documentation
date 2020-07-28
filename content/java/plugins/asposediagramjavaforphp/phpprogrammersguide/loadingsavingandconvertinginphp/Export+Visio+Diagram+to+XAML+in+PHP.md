+++
title = "Export Visio Diagram to XAML in PHP" 
description = "" 
weight = 20177 
+++

Aspose.Diagram for Java : Export Visio Diagram to XAML in PHP  

# Aspose.Diagram for Java : Export Visio Diagram to XAML in PHP


## Aspose.Diagram - Export Visio Diagram to XAML

To Export Visio Diagram to XAML using **Aspose.Diagram Java for PHP**, simply invoke **ExportToXaml** module. Here you can see example code.

**PHP Code**

{{< code lang="cs" >}}
# Call the diagram constructor to load diagram from a VSD file
$diagram = new Diagram($dataDir."Drawing.vsd");

# Save as XAML
$saveFileFormat=new SaveFileFormat();
$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;
{{< /code >}}

## Download Running Code

Download **Export Visio Diagram to XAML (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
*   [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)

