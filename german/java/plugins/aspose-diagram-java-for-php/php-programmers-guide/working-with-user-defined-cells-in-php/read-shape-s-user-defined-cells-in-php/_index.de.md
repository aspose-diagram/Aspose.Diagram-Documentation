---
title: Lesen Sie die benutzerdefinierten Zellen von Shape in PHP
type: docs
weight: 20
url: /de/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram – Benutzerdefinierte Zellen von Shape lesen**
 So lesen Sie die benutzerdefinierten Zellen von Shape mit**Aspose.Diagram Java für PHP** , einfach aufrufen**ReadUserDefinedCells** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zellen von Shape lesen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
