---
title: Удалить все макросы из Visio Diagram в PHP
type: docs
weight: 30
url: /ru/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Удалить все макросы из Visio Diagram**
 Чтобы удалить все макросы из Visio Diagram с помощью**Aspose.Diagram Java для PHP** , просто вызовите**RemoveAllMacrosFromDiagram** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Удалить все макросы из папки Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
