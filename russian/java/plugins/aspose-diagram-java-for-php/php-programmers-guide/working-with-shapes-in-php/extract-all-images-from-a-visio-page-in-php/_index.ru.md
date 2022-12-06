---
title: Извлечь все изображения со страницы Visio в PHP
type: docs
weight: 30
url: /ru/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram — Извлечение всех изображений со страницы Visio**
 Чтобы извлечь все изображения со страницы Visio, используя**Aspose.Diagram Java для PHP** , просто вызовите**Извлечь изображения** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

$typeValue=new TypeValue();

while ($i <(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

\# Filter shapes by type Foreign

if ($shape->getType()== $typeValue->FOREIGN){

\# create an image file

$fos = new FileOutputStream($dataDir."Image#{i}.bmp");

$fos->write($shape->getForeignData()->getValue());

$fos->close();

}

$i += 1;

}

print "Extracted images successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Извлечь все изображения со страницы Visio (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
