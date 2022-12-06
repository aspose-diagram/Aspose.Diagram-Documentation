---
title: Exporter Visio Diagram vers SVG en PHP
type: docs
weight: 50
url: /fr/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Exporter Visio Diagram vers SVG**
 Pour exporter Visio Diagram vers SVG en utilisant**Aspose.Diagram Java pour PHP** , invoquez simplement**Exporter vers Svg** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers SVG (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
