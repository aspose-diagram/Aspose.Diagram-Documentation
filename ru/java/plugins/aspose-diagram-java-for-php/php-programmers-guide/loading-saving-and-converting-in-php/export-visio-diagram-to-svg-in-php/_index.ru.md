---
title: Экспорт Visio Diagram в SVG в PHP
type: docs
weight: 50
url: /ru/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в SVG**
 Чтобы экспортировать Visio Diagram в SVG, используя**Aspose.Diagram Java для PHP** , просто вызовите**ЭкспорттоСвг** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в SVG (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
