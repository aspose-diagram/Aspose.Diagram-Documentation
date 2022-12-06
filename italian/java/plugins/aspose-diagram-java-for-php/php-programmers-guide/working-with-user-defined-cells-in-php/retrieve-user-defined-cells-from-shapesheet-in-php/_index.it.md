---
title: Recupera celle definite dall'utente da Shapesheet in PHP
type: docs
weight: 30
url: /it/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram - Recupera celle definite dall'utente da Shapesheet**
 Per recuperare celle definite dall'utente da Shapesheet utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**GetUserDefinedCells** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Recupera celle definite dall'utente da foglio di forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
