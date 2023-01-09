---
title: Crea una cella definita dall'utente nello ShapeSheet in PHP
type: docs
weight: 10
url: /it/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - Crea cella definita dall'utente in ShapeSheet**
 Per creare una cella definita dall'utente nello ShapeSheet utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Crea cella definita dall'utente** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Crea cella definita dall'utente in ShapeSheet (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
