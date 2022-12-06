---
title: Exportieren Sie Visio Diagram als PDF in PHP
type: docs
weight: 40
url: /de/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Visio Diagram als PDF exportieren**
 So exportieren Sie Visio Diagram in PDF mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToPdf** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
Download**Visio Diagram als PDF exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
