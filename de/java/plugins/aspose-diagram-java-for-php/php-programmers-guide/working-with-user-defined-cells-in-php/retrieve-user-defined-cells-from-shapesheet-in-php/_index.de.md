---
title: Benutzerdefinierte Zellen aus Shapesheet in PHP abrufen
type: docs
weight: 30
url: /de/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram – Benutzerdefinierte Zellen aus Shapesheet abrufen**
 So rufen Sie benutzerdefinierte Zellen aus Shapesheet ab**Aspose.Diagram Java für PHP** , einfach aufrufen**GetUserDefinedCells** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zellen aus Shapesheet abrufen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
