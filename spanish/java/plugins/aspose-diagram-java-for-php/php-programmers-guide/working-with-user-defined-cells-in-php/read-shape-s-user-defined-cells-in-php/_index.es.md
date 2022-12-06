---
title: Lea las celdas definidas por el usuario de Shape en PHP
type: docs
weight: 20
url: /es/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Leer celdas definidas por el usuario de Shape**
 Para leer las celdas definidas por el usuario de Shape usando**Aspose.Diagram Java para PHP** , simplemente invocar**Leer celdas definidas por el usuario** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Leer las celdas definidas por el usuario de Shape (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
