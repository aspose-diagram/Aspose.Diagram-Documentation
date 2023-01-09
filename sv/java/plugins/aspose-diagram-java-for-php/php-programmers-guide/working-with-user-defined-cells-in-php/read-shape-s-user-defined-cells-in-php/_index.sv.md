---
title: Läs Shapes användardefinierade celler i PHP
type: docs
weight: 20
url: /sv/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Läs Shapes användardefinierade celler**
 För att läsa Shapes användardefinierade celler med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ReadUserDefinedCells** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Läs Shapes användardefinierade celler (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
