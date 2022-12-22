---
title: Récupérer les informations de forme Visio en PHP
type: docs
weight: 70
url: /fr/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - Récupérer les informations de forme Visio**
 Pour récupérer les informations de forme Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**GetShapeInfo** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer les informations de forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
