---
title: Получить информацию о коннекторах Visio в PHP
type: docs
weight: 50
url: /ru/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Получить информацию о разъемах Visio**
 Чтобы получить информацию о соединителях Visio с помощью**Aspose.Diagram Java для PHP** , просто вызовите**GetConnectorsInfo** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$connectors = $diagram->getPages()->getPage(0)->getConnects();

$i = 0;

while ($i<sizeof($connectors->getCount())) {

$connector =$connectors->get($i);

\# Display information about the Connectors

print "From Shape ID : ".(string)$connector->getFromSheet().PHP_EOL;

print "To Shape ID : ".(string)$connector->getToSheet().PHP_EOL;

$i+=1;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о разъемах Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
