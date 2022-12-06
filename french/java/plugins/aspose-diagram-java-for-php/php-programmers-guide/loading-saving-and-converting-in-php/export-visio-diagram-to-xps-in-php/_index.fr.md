---
title: Exporter Visio Diagram vers XPS en PHP
type: docs
weight: 80
url: /fr/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Exporter Visio Diagram vers XPS**
 Pour exporter Visio Diagram vers XPS en utilisant**Aspose.Diagram Java pour PHP** , invoquez simplement**Exporter vers Xps** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers XPS (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
