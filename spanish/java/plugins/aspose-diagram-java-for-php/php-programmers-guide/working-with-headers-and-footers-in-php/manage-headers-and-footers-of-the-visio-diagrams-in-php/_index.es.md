---
title: Administre encabezados y pies de página de los diagramas Visio en PHP
type: docs
weight: 10
url: /es/java/manage-headers-and-footers-of-the-visio-diagrams-in-php/
---
## **Aspose.Diagram - Administrar encabezados y pies de página de los diagramas Visio**
 Para administrar encabezados y pies de página de los diagramas Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**Encabezados y pies de pagina** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Administrar encabezados y pies de página de los diagramas Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHeadersandFooters/HeadersAndFooters.php)
