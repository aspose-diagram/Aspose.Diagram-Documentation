---
title: Erstellen Sie eine leere Visio Diagram in PHP
type: docs
weight: 20
url: /de/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Erstellen Sie eine leere Visio Diagram**
 Erstellen Sie eine leere Visio mit Diagram**Aspose.Diagram Java für PHP** , einfach aufrufen**Diagramm erstellen** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Erstellen Sie eine leere Visio Diagram (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
