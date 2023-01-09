---
title: Récupérer des cellules définies par l'utilisateur à partir de Shapesheet en PHP
type: docs
weight: 30
url: /fr/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram - Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme**
 Pour récupérer des cellules définies par l'utilisateur à partir d'une feuille de forme à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**GetUserDefinedCells** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir . "drawing.vdx");

$pages=$diagram->getPages();

$count=0;

while($count<(int)(string)$pages->getCount()) {

$page = $pages->get($count);

$shapes = $page->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print "Name: " . $user->getNameU() . " Value: " . $user->getValue()->getVal() . " Prompt: " . $user->getPrompt()->getValue();

$j += 1;

}

break;

}

$i += 1;

}

$count += 1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Récupérer des cellules définies par l'utilisateur à partir de la feuille de forme (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
