---
title: Export Visio Diagram to PDF in PHP
type: docs
weight: 40
url: /es/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to PDF**
To Export Visio Diagram to PDF using **Aspose.Diagram Java para PHP** , simplemente invocar**Exportar a PDF** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
Descargar**Export Visio Diagram to PDF (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
