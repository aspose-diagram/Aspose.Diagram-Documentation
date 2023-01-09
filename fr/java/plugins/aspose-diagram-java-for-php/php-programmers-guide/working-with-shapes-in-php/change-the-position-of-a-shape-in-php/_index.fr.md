---
title: Changer la position d'une forme en PHP
type: docs
weight: 10
url: /fr/java/change-the-position-of-a-shape-in-php/
---
## **Aspose.Diagram - Modifier la position d'une forme**
 Pour modifier la position d'une forme à l'aide de**Aspose.Diagram Java pour PHP** , invoquez simplement**ChangeShapePosition** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 2) {

$shape->move(1, 1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ChangeShapePosition.vdx",$saveFileFormat->VDX);

print"Changed postion of a shape.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Modifier la position d'une forme (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
