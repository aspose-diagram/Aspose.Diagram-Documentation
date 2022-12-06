---
title: Экспорт Visio Diagram в PDF в PHP
type: docs
weight: 40
url: /ru/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в PDF**
 Чтобы экспортировать Visio Diagram в PDF, используя**Aspose.Diagram Java для PHP** , просто вызовите**Экспорт в PDF** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
Скачать**Экспорт Visio Diagram в PDF (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
