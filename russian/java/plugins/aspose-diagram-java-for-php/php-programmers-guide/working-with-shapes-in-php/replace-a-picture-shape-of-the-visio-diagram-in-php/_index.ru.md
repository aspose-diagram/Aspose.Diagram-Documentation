---
title: Заменить форму изображения Visio Diagram в PHP
type: docs
weight: 60
url: /ru/java/replace-a-picture-shape-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - заменить форму изображения Visio Diagram**
 Чтобы заменить форму изображения Visio Diagram с помощью**Aspose.Diagram Java для PHP** , просто вызовите**ЗаменитьPictureShape** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# convert image into bytes array

$fi = new File($dataDir."star.png");

$files=new Files();

$file_content = $files->readAllBytes($fi->toPath());

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

$typeValue=new TypeValue();

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Filter shapes by type Foreign

if ($shape->getType() == $typeValue->FOREIGN){

\# replace picture shape

$shape->getForeignData()->setValue($file_content);

}

$i+=1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ReplacePictureShape.vdx", $saveFileFormat->VDX);

print "Replaced picture shape successfully!".PHP_EOL;

{{< /highlight >}}
## **Скачать рабочий код**
 Скачать**Замените форму изображения Visio Diagram (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReplacePictureShape.php)
