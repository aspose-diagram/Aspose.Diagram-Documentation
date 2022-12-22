---
title: Export Visio Diagram to PDF in PHP
type: docs
weight: 40
url: /fr/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to PDF**
To Export Visio Diagram to PDF using **Aspose.Diagram Java pour PHP** , invoquez simplement**ExporterVersPdf** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
Télécharger**Export Visio Diagram to PDF (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
