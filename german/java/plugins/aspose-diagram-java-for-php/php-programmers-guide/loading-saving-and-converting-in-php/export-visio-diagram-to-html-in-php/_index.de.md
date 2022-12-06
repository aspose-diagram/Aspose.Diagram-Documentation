---
title: Export Visio Diagram to HTML in PHP
type: docs
weight: 20
url: /de/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToHtml** Modul. Hier sehen Sie Beispielcode.

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
 Download**Export Visio Diagram to HTML (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
