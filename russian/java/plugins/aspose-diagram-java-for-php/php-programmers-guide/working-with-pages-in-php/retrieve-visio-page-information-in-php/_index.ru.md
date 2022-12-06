---
title: Получить информацию о странице Visio в PHP
type: docs
weight: 30
url: /ru/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Получить Visio Информация о странице**
 Чтобы получить информацию о странице Visio с помощью**Aspose.Diagram Java для PHP** , просто вызовите**GetPageInfo** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о странице Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
