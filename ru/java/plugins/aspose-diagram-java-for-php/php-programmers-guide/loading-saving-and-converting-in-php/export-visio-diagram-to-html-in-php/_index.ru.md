---
title: Экспорт Visio Diagram в HTML в PHP
type: docs
weight: 20
url: /ru/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в HTML**
 Чтобы экспортировать Visio Diagram в HTML, используя**Aspose.Diagram Java для PHP** , просто вызовите**Экспорттохтмл** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в HTML (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
