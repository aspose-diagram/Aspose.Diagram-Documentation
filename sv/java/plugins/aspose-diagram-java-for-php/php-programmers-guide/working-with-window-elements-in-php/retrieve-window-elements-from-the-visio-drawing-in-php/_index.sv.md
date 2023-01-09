---
title: Hämta fönsterelement från Visio-ritningen i PHP
type: docs
weight: 30
url: /sv/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Hämta fönsterelement från Visio-ritningen**
 För att hämta fönsterelement från Visio-ritningen med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetWindowElements** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Hämta fönsterelement från Visio-ritningen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
