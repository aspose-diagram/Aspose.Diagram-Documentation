---
title: Hämta användardefinierade celler från Shapesheet i PHP
type: docs
weight: 30
url: /sv/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram - Hämta användardefinierade celler från Shapesheet**
 För att hämta användardefinierade celler från Shapesheet med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetUserDefinedCells** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Hämta användardefinierade celler från Shapesheet (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
