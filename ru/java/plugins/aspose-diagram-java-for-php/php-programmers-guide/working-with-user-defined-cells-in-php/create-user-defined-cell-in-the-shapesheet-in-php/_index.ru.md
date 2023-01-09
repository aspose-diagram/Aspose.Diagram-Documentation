---
title: Создать определяемую пользователем ячейку в ShapeSheet в PHP
type: docs
weight: 10
url: /ru/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram — Создать определяемую пользователем ячейку в таблице свойств фигуры**
 Чтобы создать определяемую пользователем ячейку в ShapeSheet, используя**Aspose.Diagram Java для PHP** , просто вызовите**CreateUserDefinedCell** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Создать определяемую пользователем ячейку в таблице свойств фигуры (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
