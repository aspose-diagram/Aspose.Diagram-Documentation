---
title: Retrieve Window Elements from the Visio Drawing in PHP
type: docs
weight: 30
url: /java/retrieve-window-elements-from-the-visio-drawing-in-php/
---

## **Aspose.Diagram - Retrieve Window Elements from the Visio Drawing**
To Retrieve Window Elements from the Visio Drawing using **Aspose.Diagram Java for PHP**, simply invoke **GetWindowElements** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Retrieve Window Elements from the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
