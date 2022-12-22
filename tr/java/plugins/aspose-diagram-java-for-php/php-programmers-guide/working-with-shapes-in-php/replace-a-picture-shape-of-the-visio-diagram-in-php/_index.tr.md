---
title: PHP'de Visio Diagram'in Resim Şeklini Değiştirme
type: docs
weight: 60
url: /tr/java/replace-a-picture-shape-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Visio Diagram'in Resim Şeklini Değiştirme**
 Visio Diagram'in Resim Şeklini Değiştirmek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Resim Şeklini Değiştir** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'in (Aspose.Diagram) Resim Şeklini Değiştirme**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReplacePictureShape.php)
