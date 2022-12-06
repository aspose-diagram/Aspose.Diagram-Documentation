---
title: Exporter Visio Diagram vers HTML en PHP
type: docs
weight: 20
url: /fr/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Exporter Visio Diagram vers HTML**
 Pour exporter Visio Diagram vers HTML en utilisant**Aspose.Diagram Java pour PHP** , invoquez simplement**ExporterVersHtml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers HTML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
