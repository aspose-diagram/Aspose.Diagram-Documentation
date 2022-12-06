---
title: Sostituisci una forma immagine di Visio Diagram in PHP
type: docs
weight: 60
url: /it/java/replace-a-picture-shape-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Sostituisci una forma immagine del Visio Diagram**
 Per sostituire una forma immagine del Visio Diagram utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**SostituisciPictureShape** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Sostituire una forma immagine del Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReplacePictureShape.php)
