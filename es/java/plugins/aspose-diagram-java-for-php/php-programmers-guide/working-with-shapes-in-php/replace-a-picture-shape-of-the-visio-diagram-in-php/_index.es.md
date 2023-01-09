---
title: Reemplace una forma de imagen de Visio Diagram en PHP
type: docs
weight: 60
url: /es/java/replace-a-picture-shape-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Reemplace una forma de imagen de Visio Diagram**
 Para reemplazar una forma de imagen de Visio Diagram usando**Aspose.Diagram Java para PHP** , simplemente invocar**ReemplazarImagenForma** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Reemplace una forma de imagen del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ReplacePictureShape.php)
