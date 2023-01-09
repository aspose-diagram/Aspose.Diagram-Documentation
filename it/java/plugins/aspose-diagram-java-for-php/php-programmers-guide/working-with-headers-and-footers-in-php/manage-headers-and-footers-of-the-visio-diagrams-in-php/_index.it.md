---
title: Gestisci intestazioni e piè di pagina dei diagrammi Visio in PHP
type: docs
weight: 10
url: /it/java/manage-headers-and-footers-of-the-visio-diagrams-in-php/
---
## **Aspose.Diagram - Gestisci intestazioni e piè di pagina dei diagrammi Visio**
 Per gestire intestazioni e piè di pagina dei diagrammi Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**HeadersAndFooters** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."drawing.vsd");

\# add page number at the right corner of header

$diagram->getHeaderFooter()->setHeaderRight("&p");

\# set text at the center

$diagram->getHeaderFooter()->setHeaderCenter("Center of the header");

\# set text at the left side

$diagram->getHeaderFooter()->setHeaderLeft("Left of the header");

\# add text at the right corner of footer

$diagram->getHeaderFooter()->setFooterRight("Right of the footer");

\# set text at the center

$diagram->getHeaderFooter()->setFooterCenter("Center of the footer");

\# set text at the left side

$diagram->getHeaderFooter()->setFooterLeft("Left of the footer");

\# set header & footer color

$color=new Color();

$diagram->getHeaderFooter()->setHeaderFooterColor($color->getRed());

\# set text font properties

$diagram->getHeaderFooter()->getHeaderFooterFont()->setItalic(1);

$diagram->getHeaderFooter()->getHeaderFooterFont()->setUnderline(0);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."HeadersAndFooters.vdx", $saveFileFormat->VDX);

print "Done with headers and footers.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Gestisci intestazioni e piè di pagina dei diagrammi Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHeadersandFooters/HeadersAndFooters.php)
