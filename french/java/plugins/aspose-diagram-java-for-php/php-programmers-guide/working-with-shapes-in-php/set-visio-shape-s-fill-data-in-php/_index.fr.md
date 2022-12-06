---
title: Définir les données de remplissage de la forme Visio en PHP
type: docs
weight: 130
url: /fr/java/set-visio-shape-s-fill-data-in-php/
---
## **Aspose.Diagram - Définir les données de remplissage de la forme Visio**
 Pour définir les données de remplissage de la forme Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**SetShapeFillData** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {

$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());

$shape->getFill()->getFillForegnd()->setValue("#ebf8df");

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);

print "Set visio shape's fill data.".PHP_EOL;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir les données de remplissage de la forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
