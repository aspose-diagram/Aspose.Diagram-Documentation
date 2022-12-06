---
title: Entfernen Sie alle Makros aus Visio Diagram in PHP
type: docs
weight: 30
url: /de/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Entfernen Sie alle Makros aus Visio Diagram**
 So entfernen Sie alle Makros aus der Visio Diagram mit**Aspose.Diagram Java für PHP** , einfach aufrufen**RemoveAllMacrosFromDiagram** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Entfernen Sie alle Makros von Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
