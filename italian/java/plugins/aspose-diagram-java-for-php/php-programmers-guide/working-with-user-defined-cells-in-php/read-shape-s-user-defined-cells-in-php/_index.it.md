---
title: Leggi le celle definite dall'utente di Shape in PHP
type: docs
weight: 20
url: /it/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Leggi le celle definite dall'utente di Shape**
 Per leggere le celle definite dall'utente di Shape utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**ReadUserDefinedCells** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Leggi celle definite dall'utente di Shape (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
