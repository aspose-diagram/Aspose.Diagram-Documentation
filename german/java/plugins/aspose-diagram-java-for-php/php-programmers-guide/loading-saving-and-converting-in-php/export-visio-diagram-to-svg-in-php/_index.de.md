---
title: Exportieren Sie Visio Diagram nach SVG in PHP
type: docs
weight: 50
url: /de/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Visio Diagram nach SVG exportieren**
 So exportieren Sie Visio Diagram in SVG mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToSvg** Modul. Hier sehen Sie Beispielcode.

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
 Download**Visio Diagram nach SVG exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
