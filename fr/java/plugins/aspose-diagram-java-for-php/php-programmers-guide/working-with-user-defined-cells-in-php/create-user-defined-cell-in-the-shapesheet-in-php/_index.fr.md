---
title: Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet en PHP
type: docs
weight: 10
url: /fr/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet**
 Pour créer une cellule définie par l'utilisateur dans la feuille ShapeSheet à l'aide**Aspose.Diagram Java pour PHP** , invoquez simplement**CreateUserDefinedCell** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir . "Drawing.vsd");

$pages=$diagram->getPages();

$i=0;

while($i<(int)(string)$pages->getCount()) {

$page = $pages->get($i);

$shapes = $page->getShapes();

$j = 0;

while ($j<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($j);

if ($shape->getNameU() == "Process") {

\# Initialize user object

$user = new User();

$user->setName("UserDefineCell");

$user->getValue()->setVal("800");

\# Add user-defined cell

$shape->getUsers()->add($user);

}

$j += 1;

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "UserDefinedCells.vdx", $saveFileFormat->VDX);

print "Created User-defined Cell in the ShapeSheet.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Créer une cellule définie par l'utilisateur dans la feuille ShapeSheet (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
