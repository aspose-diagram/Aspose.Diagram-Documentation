---
title: Exporter Visio Diagram vers une image en PHP
type: docs
weight: 30
url: /fr/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Exporter Visio Diagram vers l'image**
 Pour exporter Visio Diagram vers une image à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**Exporter vers l'image** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers l'image (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
