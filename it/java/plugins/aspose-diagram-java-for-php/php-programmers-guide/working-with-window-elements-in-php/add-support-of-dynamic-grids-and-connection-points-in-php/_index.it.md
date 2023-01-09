---
title: Aggiungi il supporto di griglie dinamiche e punti di connessione in PHP
type: docs
weight: 10
url: /it/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - Aggiunto il supporto di griglie dinamiche e punti di connessione**
 Per aggiungere il supporto di griglie dinamiche e punti di connessione utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Aggiungere DynamicGridsAndConnectionPoints** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Aggiunta del supporto di griglie dinamiche e punti di connessione (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
