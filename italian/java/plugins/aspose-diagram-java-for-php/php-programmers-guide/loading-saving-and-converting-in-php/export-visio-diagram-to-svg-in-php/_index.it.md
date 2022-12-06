---
title: Esporta Visio Diagram in SVG in PHP
type: docs
weight: 50
url: /it/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Esporta Visio Diagram in SVG**
 Per esportare Visio Diagram in SVG utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Esporta in formato Svg** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Esporta Visio Diagram in SVG (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
