---
title: Получить все слои из Visio Diagram в PHP
type: docs
weight: 20
url: /ru/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram — Получить все слои**
 Чтобы получить все слои с помощью**Aspose.Diagram Java для PHP** , просто вызовите**GetAllLayers** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить все слои из Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
