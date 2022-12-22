---
title: Définir les données de ligne de la forme Visio en PHP
type: docs
weight: 140
url: /fr/java/set-visio-shape-s-line-data-in-php/
---
## **Aspose.Diagram - Set Visio Données de ligne de forme**
 Pour définir les données de ligne de la forme Visio à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**SetShapeLineData** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && (int)(string)$shape->getID() == 1) {

$shape->getLine()->getLineColor()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(1)->getFill()->getFillForegnd()->getValue());

$shape->getLine()->getLineWeight()->setValue(0.07041666666666667);

$shape->getLine()->getRounding()->setValue(0.1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeLineData.vdx", $saveFileFormat->VDX);

print "Set visio shape's line data.".PHP_EOL;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Définir les données de ligne de la forme Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeLineData.php)
