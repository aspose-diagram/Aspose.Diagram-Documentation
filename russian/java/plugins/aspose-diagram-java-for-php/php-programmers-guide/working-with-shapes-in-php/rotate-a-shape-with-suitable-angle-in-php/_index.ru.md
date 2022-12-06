---
title: Повернуть фигуру с подходящим углом в PHP
type: docs
weight: 80
url: /ru/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Повернуть фигуру на подходящий угол**
 Чтобы повернуть фигуру на подходящий угол, используя**Aspose.Diagram Java для PHP** , просто вызовите**Повернуть фигуру** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Поворот фигуры на подходящий угол (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
