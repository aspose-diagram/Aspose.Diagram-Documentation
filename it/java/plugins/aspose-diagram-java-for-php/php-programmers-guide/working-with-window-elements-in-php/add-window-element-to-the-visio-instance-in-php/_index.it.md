---
title: Aggiungi l'elemento Window all'istanza Visio in PHP
type: docs
weight: 20
url: /it/java/add-window-element-to-the-visio-instance-in-php/
---
## **Aspose.Diagram - Aggiungi elemento finestra all'istanza Visio**
 Per aggiungere l'elemento finestra all'istanza Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**AggiungiWindowElement** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Aggiungi elemento finestra all'istanza Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddWindowElement.php)
