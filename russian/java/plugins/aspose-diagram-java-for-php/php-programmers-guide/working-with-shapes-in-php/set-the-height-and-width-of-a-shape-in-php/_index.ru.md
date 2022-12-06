---
title: Установите высоту и ширину фигуры в PHP
type: docs
weight: 120
url: /ru/java/set-the-height-and-width-of-a-shape-in-php/
---
## **Aspose.Diagram - Установка высоты и ширины фигуры**
 Чтобы установить высоту и ширину фигуры с помощью**Aspose.Diagram Java для PHP** , просто вызовите**SetShapeHeightAndWidth** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i <sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ((string)$shape->getNameU()=="Process" && (int)(string)$shape->getID()==1) {

$shape->setWidth(2 * (int)(string)$shape->getXForm()->getWidth()->getValue());

$shape->setHeight(2 * (int)(string)$shape->getXForm()->getHeight()->getValue());

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeHeightAndWidth.vdx",$saveFileFormat->VDX);

print "Set height and width of shape.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Установка высоты и ширины фигуры (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeHeightAndWidth.php)
