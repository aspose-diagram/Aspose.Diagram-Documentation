---
title: Extraire toutes les images d'une page Visio en PHP
type: docs
weight: 30
url: /fr/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram - Extraire toutes les images d'une page Visio**
 Pour extraire toutes les images d'une page Visio à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**Extraire des images** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Extraire toutes les images d'une page Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
