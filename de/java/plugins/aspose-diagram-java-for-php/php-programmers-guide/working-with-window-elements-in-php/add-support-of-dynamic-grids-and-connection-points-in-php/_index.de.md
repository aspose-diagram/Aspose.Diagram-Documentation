---
title: Unterstützung für dynamische Gitter und Verbindungspunkte in PHP hinzugefügt
type: docs
weight: 10
url: /de/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram – Unterstützung für dynamische Gitter und Verbindungspunkte hinzugefügt**
 So fügen Sie Unterstützung für dynamische Gitter und Verbindungspunkte hinzu**Aspose.Diagram Java für PHP** , einfach aufrufen**AddDynamicGridsAndConnectionPoints** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Unterstützung für dynamische Gitter und Verbindungspunkte hinzugefügt (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
