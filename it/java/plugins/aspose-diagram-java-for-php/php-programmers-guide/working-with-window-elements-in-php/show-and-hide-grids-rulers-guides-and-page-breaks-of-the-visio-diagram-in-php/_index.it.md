---
title: Mostra e nascondi griglie, righelli, guide e interruzioni di pagina di Visio Diagram in PHP
type: docs
weight: 40
url: /it/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram**
Per mostrare e nascondere griglie, righelli, guide e interruzioni di pagina di Visio Diagram utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**MostraNascondiProprietà** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# set visibility of grid

$window->setShowGrid(1);

\# set visibility of guides

$window->setShowGuides(1);

\# set visibility of rulers

$window->setShowRulers(1);

\# set visibility of page breaks

$window->setShowPageBreaks(1);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ShowHideProperties.vdx", $saveFileFormat->VDX);

print "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Mostra e nascondi griglie, righelli, guide e interruzioni di pagina del Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/ShowHideProperties.php)
