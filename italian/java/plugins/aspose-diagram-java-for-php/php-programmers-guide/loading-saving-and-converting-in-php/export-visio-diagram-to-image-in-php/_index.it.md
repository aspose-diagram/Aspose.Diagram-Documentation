---
title: Esporta Visio Diagram in Immagine in PHP
type: docs
weight: 30
url: /it/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Esporta Visio Diagram in immagine**
 Per esportare Visio Diagram nell'immagine utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Esporta in immagine** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Esporta Visio Diagram in Immagine (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
