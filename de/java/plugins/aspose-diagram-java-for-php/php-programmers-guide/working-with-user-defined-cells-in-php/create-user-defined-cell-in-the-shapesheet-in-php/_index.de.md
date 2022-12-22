---
title: Erstellen Sie eine benutzerdefinierte Zelle im ShapeSheet in PHP
type: docs
weight: 10
url: /de/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram – Benutzerdefinierte Zelle im ShapeSheet erstellen**
 So erstellen Sie eine benutzerdefinierte Zelle im ShapeSheet mit**Aspose.Diagram Java für PHP** , einfach aufrufen**CreateUserDefinedCell** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Benutzerdefinierte Zelle im ShapeSheet erstellen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
