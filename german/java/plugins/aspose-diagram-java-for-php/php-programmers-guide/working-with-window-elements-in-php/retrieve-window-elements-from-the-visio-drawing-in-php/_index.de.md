---
title: Abrufen von Fensterelementen aus der Zeichnung Visio in PHP
type: docs
weight: 30
url: /de/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Abrufen von Fensterelementen aus der Visio-Zeichnung**
 Zum Abrufen von Fensterelementen aus der Visio-Zeichnung mit**Aspose.Diagram Java für PHP** , einfach aufrufen**GetWindowElements** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$windows=$diagram->getWindows();

$i = 0;

while ($i<(int)(string)$windows->getCount()) {

$window=$windows->get($i);

print "ID: ".(string)$window->getID();

print "Type: ".(string)$window->getWindowType();

print "Window height: ".(string)$window->getWindowHeight();

print "Window width: ".(string)$window->getWindowWidth();

print"Window state: ".(string)$window->getWindowState();

$i+= 1;

}

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Abrufen von Fensterelementen aus der Zeichnung Visio (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
