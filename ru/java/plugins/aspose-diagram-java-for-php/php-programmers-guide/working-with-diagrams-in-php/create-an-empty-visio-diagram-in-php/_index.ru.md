---
title: Создайте пустой Visio Diagram в PHP
type: docs
weight: 20
url: /ru/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Создать пустой Visio Diagram**
 Чтобы создать пустой Visio Diagram с помощью**Aspose.Diagram Java для PHP** , просто вызовите**СоздатьДиаграмму** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Создайте пустой Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
