---
title: Byt ut en bildform av Visio Diagram i PHP
type: docs
weight: 60
url: /sv/java/replace-a-picture-shape-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Byt ut en bildform på Visio Diagram**
 För att ersätta en bildform på Visio Diagram med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ReplacePictureShape** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Byt ut en bildform på Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReplacePictureShape.php)
