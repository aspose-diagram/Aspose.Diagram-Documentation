---
title: Export Visio Diagram to SVG in PHP
type: docs
weight: 50
url: /de/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToSvg** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Export Visio Diagram to SVG (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
