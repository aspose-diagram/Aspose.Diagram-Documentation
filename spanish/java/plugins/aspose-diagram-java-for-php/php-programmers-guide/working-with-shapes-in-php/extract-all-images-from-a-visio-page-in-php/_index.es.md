---
title: Extraiga todas las imágenes de una página Visio en PHP
type: docs
weight: 30
url: /es/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram - Extraiga todas las imágenes de una página Visio**
 Para extraer todas las imágenes de una página Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**Extraer imágenes** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Extraiga todas las imágenes de una página Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
