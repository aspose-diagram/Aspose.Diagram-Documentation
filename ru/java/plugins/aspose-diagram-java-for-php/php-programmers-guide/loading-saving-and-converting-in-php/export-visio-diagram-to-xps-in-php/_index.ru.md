---
title: Экспорт Visio Diagram в XPS в PHP
type: docs
weight: 80
url: /ru/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в XPS**
 Чтобы экспортировать Visio Diagram в XPS, используя**Aspose.Diagram Java для PHP** , просто вызовите**Экспорттокспс** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в XPS (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
