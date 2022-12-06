---
title: Recupera gli elementi della finestra dal disegno Visio in PHP
type: docs
weight: 30
url: /it/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Recupera elementi finestra dal disegno Visio**
 Per recuperare gli elementi della finestra dal disegno Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**GetWindowElements** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Recupera elementi finestra dal disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
