---
title: Exportieren Sie Visio Diagram in XAML in PHP
type: docs
weight: 60
url: /de/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram – Visio Diagram in XAML exportieren**
 So exportieren Sie Visio Diagram in XAML mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ExportToXaml** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Visio Diagram nach XAML exportieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
