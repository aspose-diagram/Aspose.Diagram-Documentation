---
title: Lire les cellules définies par l'utilisateur de Shape en PHP
type: docs
weight: 20
url: /fr/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Lire les cellules définies par l'utilisateur de la forme**
 Pour lire les cellules définies par l'utilisateur de Shape à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**ReadUserDefinedCells** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

while($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print $user->getName() . ": " . $user->getValue()->getVal();

$j += 1;

}

break;

}

$i+=1;

}

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Lire les cellules définies par l'utilisateur de Shape (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
