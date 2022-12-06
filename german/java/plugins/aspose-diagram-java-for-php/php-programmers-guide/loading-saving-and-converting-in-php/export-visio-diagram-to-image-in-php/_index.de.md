---
title: Exportieren Sie Visio Diagram in Bild in PHP
type: docs
weight: 30
url: /de/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Visio Diagram in Bild exportieren**
 So exportieren Sie Visio Diagram in Bild mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToImage** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Diagram in Bild exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
