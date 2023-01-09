---
title: Чтение пользовательских ячеек формы в PHP
type: docs
weight: 20
url: /ru/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Чтение пользовательских ячеек фигуры**
 Чтобы прочитать пользовательские ячейки формы, используя**Aspose.Diagram Java для PHP** , просто вызовите**Реадусердефинедселлс** модуль. Здесь вы можете увидеть пример кода.

**PHP-код**

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
## **Скачать рабочий код**
 Скачать**Чтение пользовательских ячеек Shape (Aspose.Diagram)**с любого из нижеперечисленных сайтов социального кодирования:

- [Гитхаб](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
