---
title: Получить информацию о мастерах в PHP
type: docs
weight: 30
url: /ru/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Получить информацию о мастерах**
 Чтобы получить информацию о мастерах, используя**Aspose.Diagram Java для PHP** , просто вызовите**GetMasterInfo** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о мастерах (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
