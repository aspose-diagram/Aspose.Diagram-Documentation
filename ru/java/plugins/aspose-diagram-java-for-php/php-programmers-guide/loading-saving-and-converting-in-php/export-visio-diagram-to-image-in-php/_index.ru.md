---
title: Экспорт Visio Diagram в изображение в PHP
type: docs
weight: 30
url: /ru/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в изображение**
 Чтобы экспортировать Visio Diagram в изображение, используя**Aspose.Diagram Java для PHP** , просто вызовите**Экспорт в изображение** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в изображение (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
