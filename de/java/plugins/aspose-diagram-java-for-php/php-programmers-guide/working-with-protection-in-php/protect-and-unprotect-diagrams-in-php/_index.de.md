---
title: Diagramme in PHP schützen und entschützen
type: docs
weight: 20
url: /de/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram – Diagramme schützen und Schutz aufheben**
 So schützen und entschützen Sie Diagramme mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ProtectUnprotectDiagram** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vsd");

$diagram->getDocumentSettings()->setProtectBkgnds(1);

$diagram->getDocumentSettings()->setProtectMasters(1);

$diagram->getDocumentSettings()->setProtectShapes(1);

$diagram->getDocumentSettings()->setProtectStyles(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectDiagram.vdx", $saveFileFormat->VDX);

print "Applied protection on diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Diagramme zum Schützen und Aufheben des Schutzes (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
