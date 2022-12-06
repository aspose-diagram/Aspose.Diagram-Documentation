---
title: Экспорт Visio Diagram в XAML в PHP
type: docs
weight: 60
url: /ru/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - Экспорт Visio Diagram в XAML**
 Чтобы экспортировать Visio Diagram в XAML, используя**Aspose.Diagram Java для PHP** , просто вызовите**Экспорттоксамл** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Экспорт Visio Diagram в XAML (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
