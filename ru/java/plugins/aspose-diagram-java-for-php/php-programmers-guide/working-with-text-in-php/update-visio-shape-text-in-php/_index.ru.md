---
title: Обновление Visio Текст фигуры в PHP
type: docs
weight: 30
url: /ru/java/update-visio-shape-text-in-php/
---
## **Aspose.Diagram — Обновление Visio Текст формы**
Чтобы обновить текст формы Visio, используя**Aspose.Diagram Java для PHP** , просто вызовите**ОбновитьShapeText** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {

$shape->getText()->getValue()->clear();

$shape->getText()->getValue()->add(new Txt("New Text"));

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);

print "Updated shape text.".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Обновление Visio Текст формы (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
