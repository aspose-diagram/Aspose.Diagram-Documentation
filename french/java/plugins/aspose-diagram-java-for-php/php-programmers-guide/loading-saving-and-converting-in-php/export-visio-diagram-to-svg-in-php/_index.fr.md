---
title: Export Visio Diagram to SVG in PHP
type: docs
weight: 50
url: /fr/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java pour PHP** , invoquez simplement**Exporter vers Svg** module. Ici vous pouvez voir un exemple de code.

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
 Télécharger**Export Visio Diagram to SVG (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
