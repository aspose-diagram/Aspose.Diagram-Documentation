---
title: Установите Visio данные заливки формы в PHP
type: docs
weight: 130
url: /ru/java/set-visio-shape-s-fill-data-in-php/
---
## **Aspose.Diagram - Установить Visio данные заливки фигуры**
 Чтобы установить данные заливки фигуры Visio, используя**Aspose.Diagram Java для рубина** , просто вызовите**SetShapeFillData** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {

$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());

$shape->getFill()->getFillForegnd()->setValue("#ebf8df");

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);

print "Set visio shape's fill data.".PHP_EOL;

}

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Установить Visio данные заливки фигуры (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
