---
title: Fügen Sie Window Element zur Instanz Visio in PHP hinzu
type: docs
weight: 20
url: /de/java/add-window-element-to-the-visio-instance-in-php/
---
## **Aspose.Diagram – Fensterelement zur Visio-Instanz hinzugefügt**
 So fügen Sie der Instanz Visio ein Fensterelement hinzu**Aspose.Diagram Java für PHP** , einfach aufrufen**AddWindowElement** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# initialize window object

$window = new Window();

\# set window state

$windowStateValue=new WindowStateValue();

$window->setWindowState($windowStateValue->MAXIMIZED);

\# set window height

$window->setWindowHeight(500);

\# set window width

$window->setWindowWidth(500);

\# set window type

$windowTypeValue=new WindowTypeValue();

$window->setWindowType($windowTypeValue->STENCIL);

\# add window object

$diagram->getWindows()->add($window);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddWindowElement.vdx", $saveFileFormat->VDX);

print "Added window element to the visio instance.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Fensterelement zur Visio-Instanz hinzufügen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddWindowElement.php)
