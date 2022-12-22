---
title: Gérer les en-têtes et pieds de page des diagrammes Visio en PHP
type: docs
weight: 10
url: /fr/java/manage-headers-and-footers-of-the-visio-diagrams-in-php/
---
## **Aspose.Diagram - Gérer les en-têtes et pieds de page des diagrammes Visio**
 Pour gérer les en-têtes et les pieds de page des diagrammes Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**En-têtesetpieds de page** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Gérer les en-têtes et pieds de page des diagrammes Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHeadersandFooters/HeadersAndFooters.php)
