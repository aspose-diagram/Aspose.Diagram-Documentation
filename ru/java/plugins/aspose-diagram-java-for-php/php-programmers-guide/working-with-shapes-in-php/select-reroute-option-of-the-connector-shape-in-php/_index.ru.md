---
title: Выберите параметр перенаправления формы соединителя в PHP
type: docs
weight: 90
url: /ru/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram — выберите вариант перенаправления формы соединителя**
 Чтобы выбрать вариант перенаправления формы соединителя, используя**Aspose.Diagram Java для рубина** , просто вызовите**SelectRerouteOption** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Выберите вариант перенаправления формы соединителя (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
