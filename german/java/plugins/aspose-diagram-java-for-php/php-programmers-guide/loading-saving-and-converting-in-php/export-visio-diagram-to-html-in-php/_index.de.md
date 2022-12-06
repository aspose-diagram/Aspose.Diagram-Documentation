---
title: Exportieren Sie Visio Diagram in HTML in PHP
type: docs
weight: 20
url: /de/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Visio Diagram in HTML exportieren**
 So exportieren Sie Visio Diagram in HTML mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToHtml** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Diagram in HTML exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
