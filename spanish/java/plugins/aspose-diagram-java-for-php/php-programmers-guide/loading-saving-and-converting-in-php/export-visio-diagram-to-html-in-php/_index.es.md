---
title: Exportar Visio Diagram a HTML en PHP
type: docs
weight: 20
url: /es/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Exportar Visio Diagram a HTML**
 Para exportar Visio Diagram a HTML usando**Aspose.Diagram Java para PHP** , simplemente invocar**Exportar a HTML** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a HTML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
