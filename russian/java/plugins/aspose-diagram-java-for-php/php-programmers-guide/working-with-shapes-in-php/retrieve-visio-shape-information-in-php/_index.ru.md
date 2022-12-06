---
title: Получить Visio информацию о форме в PHP
type: docs
weight: 70
url: /ru/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram — Получить информацию о форме Visio**
 Чтобы получить информацию о форме Visio, используя**Aspose.Diagram Java для PHP** , просто вызовите**GetShapeInfo** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Получить информацию о форме Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
